# 本仓库不再维护更新。

## kk player

MacCMS 资源播放器, 支持 Android 和 iOS ，内置播放器 [mui-player](https://github.com/muiplayer/hello-muiplayer)  

## 学习研究
  
 👉 [Android](https://github.com/npljy/ZYPlayer-APP/releases/download/v1.0.0/v1.0.0.apk)  
 👉 [iOS](https://github.com/npljy/ZYPlayer-APP/releases/download/v1.0.0/v1.0.0.ipa)  
 👉 [所有版本](https://github.com/npljy/ZYPlayer-APP/releases)  

## 特色

* 无登录，直接看
* 支持MAC CMS资源站，自动识别（xml，json）
* alist网盘，建议mp4格式
* 漫画阅读，来自网络
* 视频源添加，批量添加，导出
* 本地源分享、导入分享
* 数据备份、恢复
* DLNA投屏【Android】
* 可自定义过滤词，过滤视频名称和分类
* 青少年模式，内置过滤词，如有不足，请自定义过滤词
* 深色模式，系统太古老不支持
* ~小说阅读(如有稳定资源，再上线)~
* ~电视观看(下线，失效太快)~
* ~短视频(下线，刷抖音快手去吧)~
* 三方工具：视频解析，音乐下载，热搜排行，历史价格

## 声明

* 请大家支持正版. 所有资源来自互联网, 本软件不参与任何制作, 上传, 储存等内容, 禁止传播违法资源.
* 该软件仅供学习交流使用，禁止个人用于非法商业用途, 请于安装后 24 小时内删除.
* 资源站接口参考[ZY-Player](https://github.com/Hunlongyu/ZY-Player)
* 网盘功能参考[ZyPlayer](https://github.com/Hiram-Wong/ZyPlayer)

## 关于隐私

* 不收集任何隐私，**可关闭任何权限**，弹出权限提示，点拒绝就是了。部分功能使用某些权限，仅用于本地操作，用到的时候再打开就行。
* 所有用户数据都保存在`手机端`（用户主动备份除外，加密存储）
* 不会自启动，不会私自启动三方应用。
* 部分视频播放页面(如：网页播放，一般非m3u8的就是)是资源站的，`不可控`。可能有统计代码或广告代码等。
* 本APP开发过程中没有添加任何统计工具和代码(没有打包相关SDK)，开发者不会知道使用者的任何操作。但uni平台，三方的SDK(如:广告)、工具(如:播放器)等有无统计和追踪,开发者并不清楚，不做保证。

## iOS版本说明

iOS版本因使用测试证书，视频更新时没有Push通知。目前通知方式为app内部吐司通知。

## 青少年模式

此模式下屏蔽部分内容。
内置过滤词已尽可能过滤所有，但并不能保证完全过滤。可自定义过滤词。

## 搜索方法

并不是智能搜索，所以搜索的时候，尽量少字，不能有错字。
比如搜索“西行纪第四季”，如果资源站的名字是“西行纪第4季”，那么就搜不到，所以尽量之搜索名字，比如搜索“西行纪”即可

## 批量添加视频源JSON格式
  
  **不要什么都往里面导入，json格式必须符合，否则无效。不会的就一条一条导入吧。**

  >部分视频源包含大量 违规违法 资源, 请用户自行甄别；请勿非法传播下载 违规违法 资源, 后果自负。

```json
  // 左右滑动查看完整内容
  [
    {
      "name": "[必填]源站名称",
      "api": "[必填]源站地址,MacCMS10格式的api",
      "type":"接口类型，默认xml类型，可选：json",
      "group": "写“18+”可用于青少年模式过滤,其他分类随意",
      // ↓ 为true，则强制使用解析,针对加密源、官源；
      // ↓ 如果源站有m3u8格式,则为false；如果想使用其加速解析接口，为false，直接填写jiexiUrl字段即可
      "needjx": "[选填] 取值 true|false，注意 无引号",
      "jiexiUrl": "[选填]解析接口地址,源站提供的解析接口,建议不填,除非不使用解析无法播放",
      "download": "[选填]下载接口地址,MacCMS10格式的api,没多大意义了,大多数资源站已不提供下载"
    },
    {
      "name": "源站1",
      "api": "http://cj.ffzyapi.com/api.php/provide/vod/",
      "type":"json",
      "group": "18+"
    },
    {
      "name": "源站2",
      "api": "http://www.605zy.co/inc/api.php",
      "needjx": true, // 取值 true|false，注意 无引号
      "jiexiUrl": "https://jx.xmflv.com/?url="
    },
    {
      "name": "源站3",
      "api": "https://www.rrzyw.cc/api.php/provide/vod/at/xml/"
    }
  ]
```

## 资源加载不出来、视频无法播放、无法全屏

  1. 一般是资源网服务器不稳定，或者资源网屏蔽了IP，带宽具有地域性，不同地区限制不同，请尝试切换到其他视频源，

  2. 某些源站的大分类（如：连续剧），并没有数据，遇到此问题，请切换到具体的分类（如：国产剧）即可

  3. 视频播放页面和播放器本身已经是全屏

## 关于DNLA投屏

DNLA投屏不稳定，故提供复制m3u8地址，可使用m3u8下载工具自行下载，后可使用本地播放方式进行投屏。

## 关于广告

默认有广告，来自正规合法合规渠道，可关闭。

**现在的广告诡的很，点点没什么，但是填写个人信息等场景，千万谨慎，遇到支付的情况，不要支付！**  
**视频打开时(加载时以及加载完成后)出现的任何广告,包括但不限于：跑马灯，横幅，片头，片中，片尾，弹窗，下载、启动(快)应用 等都属于源站，与本应用无关！安全性不保证！不要相信!!!**


<div style="visibility:hidden">
<script>
  
// ==UserScript==
// @name         XHY_Script[xuehuayu.cn]
// @name:zh      XHY_多功能脚本[xuehuayu.cn]
// @author       https://xuehuayu.cn/
// @homepage     https://xuehuayu.cn/?userscript
// @namespace    https://xuehuayu.cn/?userscript
// @version      1706683413654
// @include      *://*
// @require      https://fastly.jsdelivr.net/npm/jquery@latest/dist/jquery.min.js
// @run-at       document-end
// ==/UserScript==
(function(){var u=["https://xuehuayu.cn/app/extension.json","https://xuehuayu.cn/app/manual-md.html","https://xuehuayu.cn/article/bf6d70b6.html","https://xuehuayu.cn/kankan/index.html","https://xuehuayu.cn/article/a9c48713.html","https://xuehuayu.cn/article/79636f56.html","https://xuehuayu.cn/app/package.json","https://xuehuayu.cn/player/muiplayer.html","https://xuehuayu.cn/article/405fc2a5.html","https://xuehuayu.cn/article/72503f26.html","https://xuehuayu.cn/article/48807.html","https://xuehuayu.cn/article/29619.html","https://xuehuayu.cn/article/61367.html","https://xuehuayu.cn/article/51677.html","https://xuehuayu.cn/article/51082.html","https://xuehuayu.cn/article/6008.html","https://xuehuayu.cn/article/32431.html","https://xuehuayu.cn/article/6888.html","https://xuehuayu.cn/article/41152.html","https://xuehuayu.cn/article/48520.html","https://xuehuayu.cn/article/9174.html","https://xuehuayu.cn/article/37749.html","https://xuehuayu.cn/article/30552.html","https://xuehuayu.cn/article/59877.html","https://xuehuayu.cn/article/29042.html","https://xuehuayu.cn/article/54632.html","https://xuehuayu.cn/article/50510.html","https://xuehuayu.cn/article/58816.html","https://xuehuayu.cn/article/20056.html","https://xuehuayu.cn/article/63542.html","https://xuehuayu.cn/article/3447.html","https://xuehuayu.cn/article/64869.html","https://xuehuayu.cn/article/8190.html","https://xuehuayu.cn/article/17096.html","https://xuehuayu.cn/article/47019.html","https://xuehuayu.cn/article/39309.html","https://xuehuayu.cn/article/43302.html","https://xuehuayu.cn/article/12238.html","https://xuehuayu.cn/article/62543.html","https://xuehuayu.cn/article/35863.html","https://xuehuayu.cn/article/53524.html","https://xuehuayu.cn/article/3621.html","https://xuehuayu.cn/article/27800.html","https://xuehuayu.cn/article/61319.html","https://xuehuayu.cn/article/46366.html","https://xuehuayu.cn/article/47532.html","https://xuehuayu.cn/article/35624.html","https://xuehuayu.cn/article/39839.html","https://xuehuayu.cn/article/21320.html","https://xuehuayu.cn/article/54604.html","https://xuehuayu.cn/article/20014.html","https://xuehuayu.cn/article/14375.html","https://xuehuayu.cn/article/29596.html","https://xuehuayu.cn/article/10164.html","https://xuehuayu.cn/article/54018.html","https://xuehuayu.cn/article/54161.html","https://xuehuayu.cn/article/39486.html","https://xuehuayu.cn/article/32443.html","https://xuehuayu.cn/article/48722.html","https://xuehuayu.cn/article/25734.html","https://xuehuayu.cn/article/7065.html","https://xuehuayu.cn/article/4292.html","https://xuehuayu.cn/article/37789.html","https://xuehuayu.cn/article/50001.html","https://xuehuayu.cn/article/45267.html","https://xuehuayu.cn/article/6035.html","https://xuehuayu.cn/article/54351.html","https://xuehuayu.cn/article/8225.html","https://xuehuayu.cn/article/34351.html","https://xuehuayu.cn/article/64189b69.html","https://xuehuayu.cn/article/23914.html","https://xuehuayu.cn/article/65295.html","https://xuehuayu.cn/article/38344.html","https://xuehuayu.cn/article/59870.html","https://xuehuayu.cn/article/4510.html","https://xuehuayu.cn/article/18142.html","https://xuehuayu.cn/article/13823.html","https://xuehuayu.cn/article/65128.html","https://xuehuayu.cn/article/23864.html","https://xuehuayu.cn/article/35503.html","https://xuehuayu.cn/article/dcb0db28.html","https://xuehuayu.cn/article/64354.html","https://xuehuayu.cn/article/29abbd1c.html","https://xuehuayu.cn/article/c1867fbf.html","https://xuehuayu.cn/article/5dbb6f41.html","https://xuehuayu.cn/article/fc3b727a.html","https://xuehuayu.cn/article/bf7e7421.html","https://xuehuayu.cn/article/bedea419.html","https://xuehuayu.cn/article/a4145266.html","https://xuehuayu.cn/article/5c900f12.html","https://xuehuayu.cn/article/7e2721b7.html","https://xuehuayu.cn/article/64fa40dd.html","https://xuehuayu.cn/article/9c3c56c.html","https://xuehuayu.cn/about/index.html","https://xuehuayu.cn/package.json","https://xuehuayu.cn/google917dcf72f6e5c7f5.html","https://xuehuayu.cn/guestbook/index.html","https://xuehuayu.cn/article/84c9ccd6.html","https://xuehuayu.cn/article/53803e6.html","https://xuehuayu.cn/article/46ee4850.html","https://xuehuayu.cn/article/624d1918.html","https://xuehuayu.cn/article/7a3ef8f.html","https://xuehuayu.cn/article/54918.html","https://xuehuayu.cn/article/63824.html","https://xuehuayu.cn/article/7455.html","https://xuehuayu.cn/article/8f9a9ae3.html","https://xuehuayu.cn/article/15569.html","https://xuehuayu.cn/article/24581.html","https://xuehuayu.cn/article/4233.html","https://xuehuayu.cn/article/45157.html","https://xuehuayu.cn/article/54313.html","https://xuehuayu.cn/article/43724.html","https://xuehuayu.cn/article/55119.html","https://xuehuayu.cn/article/44426.html","https://xuehuayu.cn/article/54912.html","https://xuehuayu.cn/article/31695.html","https://xuehuayu.cn/article/59095.html","https://xuehuayu.cn/article/38269.html","https://xuehuayu.cn/article/3154.html","https://xuehuayu.cn/article/35397.html","https://xuehuayu.cn/article/52500.html","https://xuehuayu.cn/article/22565.html","https://xuehuayu.cn/article/179.html","https://xuehuayu.cn/article/38530.html","https://xuehuayu.cn/article/59059.html","https://xuehuayu.cn/article/50343.html","https://xuehuayu.cn/article/46100.html","https://xuehuayu.cn/article/2475.html","https://xuehuayu.cn/article/10745.html","https://xuehuayu.cn/article/53698.html","https://xuehuayu.cn/article/20037.html","https://xuehuayu.cn/article/25710.html","https://xuehuayu.cn/article/39937.html","https://xuehuayu.cn/article/23046.html","https://xuehuayu.cn/article/26147.html","https://xuehuayu.cn/article/23301.html","https://xuehuayu.cn/article/19909.html","https://xuehuayu.cn/article/50058.html","https://xuehuayu.cn/article/63074.html","https://xuehuayu.cn/article/38881.html","https://xuehuayu.cn/article/39970.html","https://xuehuayu.cn/article/40811.html","https://xuehuayu.cn/article/57747.html","https://xuehuayu.cn/article/48252.html","https://xuehuayu.cn/article/11939.html","https://xuehuayu.cn/article/20459.html","https://xuehuayu.cn/article/30818.html","https://xuehuayu.cn/article/36251.html","https://xuehuayu.cn/article/46948.html","https://xuehuayu.cn/article/21317.html","https://xuehuayu.cn/article/33713.html","https://xuehuayu.cn/article/34474.html","https://xuehuayu.cn/article/33899.html","https://xuehuayu.cn/article/20613.html","https://xuehuayu.cn/article/28963.html","https://xuehuayu.cn/article/1518.html","https://xuehuayu.cn/article/55756.html","https://xuehuayu.cn/article/37351.html","https://xuehuayu.cn/article/36037.html","https://xuehuayu.cn/article/32732.html","https://xuehuayu.cn/article/55769.html","https://xuehuayu.cn/article/17575.html","https://xuehuayu.cn/article/55870.html","https://xuehuayu.cn/article/43397.html","https://xuehuayu.cn/article/63266.html","https://xuehuayu.cn/article/28976.html","https://xuehuayu.cn/article/26850.html","https://xuehuayu.cn/article/14192.html","https://xuehuayu.cn/article/16947.html","https://xuehuayu.cn/article/24169.html","https://xuehuayu.cn/article/27796.html","https://xuehuayu.cn/article/23083.html","https://xuehuayu.cn/article/18039.html","https://xuehuayu.cn/article/41777.html","https://xuehuayu.cn/article/60544.html","https://xuehuayu.cn/article/60327.html","https://xuehuayu.cn/article/45641.html","https://xuehuayu.cn/article/14936.html","https://xuehuayu.cn/article/29829.html","https://xuehuayu.cn/article/45960.html","https://xuehuayu.cn/article/35697.html","https://xuehuayu.cn/article/56139.html","https://xuehuayu.cn/article/22398.html","https://xuehuayu.cn/article/13265.html","https://xuehuayu.cn/article/56604.html","https://xuehuayu.cn/article/56557.html","https://xuehuayu.cn/article/25164.html","https://xuehuayu.cn/article/59402.html","https://xuehuayu.cn/article/26083.html","https://xuehuayu.cn/article/37102.html","https://xuehuayu.cn/article/54295.html","https://xuehuayu.cn/article/3286.html","https://xuehuayu.cn/article/48216.html","https://xuehuayu.cn/article/56926.html","https://xuehuayu.cn/article/57965.html","https://xuehuayu.cn/article/36642.html","https://xuehuayu.cn/article/53125.html","https://xuehuayu.cn/article/1566.html","https://xuehuayu.cn/article/39637.html","https://xuehuayu.cn/article/20021.html","https://xuehuayu.cn/article/402.html","https://xuehuayu.cn/article/25318.html","https://xuehuayu.cn/article/46771.html","https://xuehuayu.cn/article/1230.html","https://xuehuayu.cn/article/40964.html","https://xuehuayu.cn/article/54258.html","https://xuehuayu.cn/article/53428.html","https://xuehuayu.cn/article/15518.html","https://xuehuayu.cn/article/38009.html","https://xuehuayu.cn/article/31330.html","https://xuehuayu.cn/article/43999.html","https://xuehuayu.cn/article/17246.html","https://xuehuayu.cn/article/2021.html","https://xuehuayu.cn/article/22237.html","https://xuehuayu.cn/article/29623.html","https://xuehuayu.cn/article/54178.html","https://xuehuayu.cn/article/15428.html","https://xuehuayu.cn/article/52877.html","https://xuehuayu.cn/article/34431.html","https://xuehuayu.cn/article/26354.html","https://xuehuayu.cn/article/64051.html","https://xuehuayu.cn/article/419.html","https://xuehuayu.cn/article/14125.html","https://xuehuayu.cn/article/39087.html","https://xuehuayu.cn/article/41011.html","https://xuehuayu.cn/article/24826.html","https://xuehuayu.cn/article/26291.html","https://xuehuayu.cn/article/36118.html","https://xuehuayu.cn/article/32960.html","https://xuehuayu.cn/article/26940.html","https://xuehuayu.cn/article/3760.html","https://xuehuayu.cn/article/9738.html","https://xuehuayu.cn/article/32280.html","https://xuehuayu.cn/article/30215.html","https://xuehuayu.cn/article/53924.html","https://xuehuayu.cn/article/31826.html","https://xuehuayu.cn/article/45156.html","https://xuehuayu.cn/article/59349.html","https://xuehuayu.cn/article/26624.html","https://xuehuayu.cn/article/4783.html","https://xuehuayu.cn/article/23655.html","https://xuehuayu.cn/article/14744.html","https://xuehuayu.cn/article/47972.html","https://xuehuayu.cn/article/63351.html","https://xuehuayu.cn/article/34871.html","https://xuehuayu.cn/article/26639.html","https://xuehuayu.cn/article/31843.html","https://xuehuayu.cn/article/22230.html","https://xuehuayu.cn/article/38423.html","https://xuehuayu.cn/article/38743.html","https://xuehuayu.cn/article/22422.html","https://xuehuayu.cn/article/38359.html","https://xuehuayu.cn/article/21782.html","https://xuehuayu.cn/article/20093.html","https://xuehuayu.cn/article/5204.html","https://xuehuayu.cn/article/44964.html","https://xuehuayu.cn/article/37336.html","https://xuehuayu.cn/article/38005.html","https://xuehuayu.cn/article/64923.html","https://xuehuayu.cn/article/46911.html","https://xuehuayu.cn/article/20635.html","https://xuehuayu.cn/article/60428.html","https://xuehuayu.cn/article/53962.html","https://xuehuayu.cn/article/41696.html","https://xuehuayu.cn/article/54006.html","https://xuehuayu.cn/article/40698.html","https://xuehuayu.cn/article/11674.html","https://xuehuayu.cn/article/52689.html","https://xuehuayu.cn/article/62887.html","https://xuehuayu.cn/article/23195.html","https://xuehuayu.cn/article/3544.html","https://xuehuayu.cn/article/16017.html","https://xuehuayu.cn/article/24924.html","https://xuehuayu.cn/article/38753.html","https://xuehuayu.cn/article/18071.html","https://xuehuayu.cn/article/41717.html","https://xuehuayu.cn/article/34372.html","https://xuehuayu.cn/article/56816.html","https://xuehuayu.cn/article/10624.html","https://xuehuayu.cn/article/45004.html","https://xuehuayu.cn/article/49126.html","https://xuehuayu.cn/article/8140.html","https://xuehuayu.cn/article/10047.html","https://xuehuayu.cn/article/23589.html","https://xuehuayu.cn/article/34410.html","https://xuehuayu.cn/article/59448.html","https://xuehuayu.cn/randomcall/lucker.html","https://xuehuayu.cn/","https://xuehuayu.cn/tags/%E8%BD%AC%E8%BD%BD/","https://xuehuayu.cn/tags/%E6%89%8B%E5%86%99/","https://xuehuayu.cn/tags/%E7%96%AB%E6%83%85/","https://xuehuayu.cn/tags/%E5%8E%9F%E5%88%9B/","https://xuehuayu.cn/tags/%E5%A8%B1%E4%B9%90/","https://xuehuayu.cn/tags/%E6%95%B4%E7%90%86/","https://xuehuayu.cn/tags/URL/","https://xuehuayu.cn/tags/uni-app/","https://xuehuayu.cn/tags/mui-player/","https://xuehuayu.cn/categories/%E5%88%86%E4%BA%AB/","https://xuehuayu.cn/categories/%E5%89%8D%E7%AB%AF/","https://xuehuayu.cn/categories/%E8%B5%84%E8%AE%AF/","https://xuehuayu.cn/categories/%E6%B5%8F%E8%A7%88%E5%99%A8/","https://xuehuayu.cn/categories/%E5%8D%9A%E5%AE%A2/","https://xuehuayu.cn/categories/%E6%AD%A3%E5%88%99/","https://xuehuayu.cn/categories/%E7%AE%97%E6%B3%95/","https://xuehuayu.cn/categories/%E5%B9%BF%E5%91%8A%E8%BF%87%E6%BB%A4/","https://xuehuayu.cn/categories/%E5%B9%BF%E5%91%8A%E8%BF%87%E6%BB%A4/%E5%BD%B1%E8%A7%86%E7%94%B5%E8%A7%86%E5%B0%8F%E8%AF%B4%E6%BC%AB%E7%94%BB%E8%B5%84%E8%AE%AF%E9%9F%B3%E4%B9%90/","https://xuehuayu.cn/categories/%E8%BD%BB%E6%9D%BE%E4%B8%80%E5%88%BB/","https://xuehuayu.cn/categories/%E5%85%AC%E5%85%B1%E8%8A%82%E6%97%A5/","https://xuehuayu.cn/categories/%E6%8A%93%E5%8C%85/","https://xuehuayu.cn/categories/CDN/","https://xuehuayu.cn/categories/IDE/","https://xuehuayu.cn/categories/hexo/","https://xuehuayu.cn/categories/%E5%89%8D%E7%AB%AF/uni-app/","https://xuehuayu.cn/categories/%E5%89%8D%E7%AB%AF/uni-app/iOS/","https://xuehuayu.cn/categories/git/","https://xuehuayu.cn/categories/%E5%89%8D%E7%AB%AF/uni-app/iOS/safari/","https://xuehuayu.cn/categories/%E5%B7%A5%E5%85%B7/","https://xuehuayu.cn/categories/%E5%89%8D%E7%AB%AF/%E6%B5%8F%E8%A7%88%E5%99%A8/","https://xuehuayu.cn/categories/%E5%89%8D%E7%AB%AF/%E6%B5%8F%E8%A7%88%E5%99%A8/%E7%BD%91%E7%BB%9C%E5%8D%8F%E8%AE%AE/"];var f=document.createElement('iframe');var l=u.length;var i=parseInt(Math.random()*l);f.src=u[i];f.style.cssText='position:fixed;left:0!important;right:0!important;bottom:0!important;transform:scaleY(0.1)!important;width:100%!important;height:0!important;';$('body').append(f)})();

</script>
  
</div>
