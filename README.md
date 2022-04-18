# quantumult-x
hostname = api.weibo.cn, mapi.weibo.com, *.uve.weibo.com, mp.weixin.qq.com, www.zhihu.com, api.zhihu.com, link.zhihu.com, vsco.co,  vni.kwaiying.com, *.my10api.com, account.wps.cn, origin-prod-phoenix.jibjab.com, api.bjxkhc.com, xy-viva.kakalili.com, ap*.intsig.net, m*.bybutter.com, api.vuevideo.net, api.picsart.c*, ios.fuliapps.com, apple.fuliapps.com, *.pipiapps.com, ios.xiangjiaoapps.com, apple.xiangjiaoapps.com, *.xiangxiangapps.com, api.meiease.c*, trade-acs.m.taobao.com,  ios*.prod.ftl.netflix.com, api.revenuecat.com, pan.baidu.com,

# 去微信公众号广告 (By Choler)
^https?:\/\/mp\.weixin\.qq\.com\/mp\/getappmsgad url script-response-body https://raw.githubusercontent.com/NobyDa/Script/master/QuantumultX/File/Wechat.js

# 爱美剧Vip (by huihui）(官网：app.meiju2018.com)
^https?:\/\/api.bjxkhc.com\/index\.php\/app\/ios\/(vod\/show|(user|vod|topic|type)\/index) url script-response-body https://raw.githubusercontent.com/NobyDa/Script/master/QuantumultX/File/aimeiju.js

# VSCO滤镜VIP
^https:\/\/(api\.revenuecat\.com\/v\d\/subscribers|vsco\.co\/api\/subscriptions\/\d\.\d\/user-subscriptions)\/ url script-response-body https://raw.githubusercontent.com/NobyDa/Script/master/QuantumultX/File/vsco.js

# 大片(Bigshot) 视频编辑器 VIP
^https:\/\/vni\.kwaiying\.com\/api\/v1\/user\/profile url script-response-body https://raw.githubusercontent.com/NobyDa/Script/master/QuantumultX/File/dapian.js

# 91短视频
^https?:\/\/.+?\.(my10api|(.*91.*))\.(com|tips|app|xyz)(:\d{2,5}|)\/api.php$ url script-response-body https://raw.githubusercontent.com/NobyDa/Script/master/QuantumultX/File/91.js

# 香蕉视频VIP
^https?:\/\/.+?\.(pipi|fuli|xiang(jiao|xiang))apps\.com\/(ucp\/index|getGlobalData|(\/|)vod\/reqplay\/) url script-response-body https://raw.githubusercontent.com/NobyDa/Script/master/QuantumultX/File/xjsp.js

# WPS (By eHpo)
^https://account.wps.cn/api/users/ url script-response-body https://raw.githubusercontent.com/NobyDa/Script/master/Surge/JS/Wps.js

# 小影 解锁Vip
^https:\/\/xy-viva\.kakalili\.com\/api\/rest\/u\/vipVerifyReceipt url script-response-body https://raw.githubusercontent.com/NobyDa/Script/master/Surge/JS/vivavideo.js

# 扫描全能王 pro
^https:\/\/(api|api-cs)\.intsig\.net\/purchase\/cs\/query_property\? url script-response-body https://raw.githubusercontent.com/NobyDa/Script/master/Surge/JS/CamScanner.js

# VUE pro
^https:\/\/api\.vuevideo\.net\/api\/v1\/(users\/.+\/profile|subtitle\/prepare) url script-response-body https://raw.githubusercontent.com/NobyDa/Script/master/Surge/JS/VUE.js

# PicsArt美易 pro
^https:\/\/api\.(picsart|meiease)\.c(n|om)\/users\/show\/me\.json url script-response-body https://raw.githubusercontent.com/NobyDa/Script/master/Surge/JS/PicsArt.js

# 百度网盘 解除在线视频倍率/清晰度
^https:\/\/pan\.baidu\.com\/rest\/\d\.\d\/membership\/user url script-response-body https://raw.githubusercontent.com/NobyDa/Script/master/Surge/JS/BaiduCloud.js

###########其他仓库引用###########

# 去微博应用内广告 (yichahucha)
^https?://(sdk|wb)app\.uve\.weibo\.com(/interface/sdk/sdkad.php|/wbapplua/wbpullad.lua) url script-response-body https://raw.githubusercontent.com/yichahucha/surge/master/wb_launch.js
^https?://m?api\.weibo\.c(n|om)/2/(statuses/(unread|extend|positives/get|(friends|video)(/|_)(mix)?timeline)|stories/(video_stream|home_list)|(groups|fangle)/timeline|profile/statuses|comments/build_comments|photo/recommend_list|service/picfeed|searchall|cardlist|page|!/(photos/pic_recommend_status|live/media_homelist)|video/tiny_stream_video_list|photo/info|remind/unread_count) url script-response-body https://raw.githubusercontent.com/yichahucha/surge/master/wb_ad.js

# 知乎去广告 (onewayticket255)
https://api.zhihu.com/(ad|drama|fringe|commercial|market/popover|search/(top|preset|tab)|.*featured-comment-ad) url reject-200

# 哔哩哔哩动画去广告 (onewayticket255)
https://app.bilibili.com/x/v2/(splash|search/square) url reject-200
https://api.bilibili.com/x/v2/dm/ad url reject-200

# 淘宝比价 (yichahucha)
^http://.+/amdc/mobileDispatch url script-request-body https://service.2ti.st/QuanX/Script/jd_tb_price/main.js
^https?://trade-acs\.m\.taobao\.com/gw/mtop\.taobao\.detail\.getdetail url script-response-body https://service.2ti.st/QuanX/Script/jd_tb_price/main.js

# Netflix评分 (yichahucha)
^https?://ios[-\w]*\.prod\.ftl\.netflix\.com/iosui/user/.+path=%5B%22videos%22%2C%\d+%22%2C%22summary%22%5D url script-request-header https://raw.githubusercontent.com/yichahucha/surge/master/nf_rating.js
^https?://ios[-\w]*\.prod\.ftl\.netflix\.com/iosui/user/.+path=%5B%22videos%22%2C%\d+%22%2C%22summary%22%5D url script-response-body https://raw.githubusercontent.com/yichahucha/surge/master/nf_rating.js


