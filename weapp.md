---
title: 小程序
date: 2017-01-13 12:12:00
categories: Project
tags:
 - Weapp
---

简单学习了下，写了个[盛世华安小程序](https://github.com/yaoshanliang/weapp-ssha)，已审核上线。

使用微信开发者工具可以新建一个**quickstart**的项目，扫了一遍目录结构和代码，发现这家伙长的跟**react native**还挺像的，不过没有对android和ios分开处理，毕竟小程序是基于微信，跨平台的处理交由微信就行了，这样一来小程序的门槛就比react native低很多了。

<!-- more -->

第一版采用的是静态页面，主要是为了走一遍流程。不过提交后，发现了一个小bug，想修复后重新提交。但是，当前审核中的小程序是不能撤销的，也就是必须等当前版本审核完成才能提交新的版本。

第二版采用的是动态页面，通过wordpress的[JSON API](https://wordpress.org/plugins/json-api/)插件提供公司官网数据，然后调用小程序的`wx.request()`去获取数据，并且`wx.request`发起的是HTTPS请求，需要在小程序的开发者平台中添加可访问的域名，当然开发版可以在微信开发者工具中勾选*“开发环境不校验请求域名以及TLS版本”*。

另一点需要提到的是，小程序还没有提供webview的api，这也就需要第三方的库，开发中采用的是[wxParse](https://github.com/icindy/wxParse)，调用`WxParse.wxParse('article', 'html', article, that, 5);
`即可。

---
* 扫码访问
![](http://iat.net.cn/images/weapp-ssha-qrcode.jpg)

* 预览
![](http://iat.net.cn/images/weapp-ssha-1.png)
![](http://iat.net.cn/images/weapp-ssha-log.jpeg)

小程序发布后，有说是前端开发者的春天，也有抨击小程序的，这里不做评论，吃瓜移步[知乎](https://www.zhihu.com/topic/20061410/hot)。

