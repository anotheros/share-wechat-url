# share-wechat-url
共享微信公众号url


## 原因

因为大家都爬微信的文章，而且大多是因为文章的url问题，为此我做了个共享计划。
大家都分享自己的url。

微信文章url 正则表达式 `((http|https)://mp\.weixin\.qq.com/s\?__biz=\w{14}==&mid=\d{9}.+?&sn=\w{32})`

## 思路如下。

各自抓到的url，分享到群里，然后其他人复制就ok。

### 技术方法。

微信web协议 的 wechat-robot（或者 itchat）+ slack 频道 + slack api。

### 流程如下。

发送（共享过程）：微信关注公众号，公众号 发来推送的文章，wechat-robot 收到推送的文章url，程序将 url 发送到slack 的webhooks 地址，该地址对应 分享微信url的 slack 频道 （类似qq群）。

接收（拿到别人共享内容）：slack bot （类似一个qq号）收到url，slack bot 将url地址发送给对应的业务地址。

代码已经写完。正在内测。


[代码](https://github.com/zhangshanhai/weixinbot)
