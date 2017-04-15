# smart_login
本项目用于研究和分享各大网站的模拟登陆方式,主要使用selenium+phantomjs或者直接登录的方式,语言采用Python


## 关于

由于工作需要，研究了一段时间的新浪微博登陆方式，在网上也查看了很多别人的经验，但是有相当一部分都是转载而且代码老旧，所以便有了这个repo。

模拟登陆基本采用的是直接登录或者使用selenium+webdriver的方式，有的网站直接登录难度很大，比如qq空间，如果采用selenium就相对轻松一些。

虽然在登录的时候采用的是selenium,为了效率，我们可以在登录过后得到的cookie维护起来，然后调用requests或者scrapy等进行数据采集，这样数据采集的速度可以得到保证。

下面是已经实现和待实现的目标

- [x] 微博
- [x] 知乎
- [x] QQ空间
- [x] 京东
- [x] 163邮箱
- [x] CSDN
- [ ] 淘宝
- [x] 百度
- [ ] 果壳
- [ ] 拉钩

其中比较典型的是微博这一类的模拟登陆，会用到RSA、Base64等加密和编码算法，关于它的分析过程，我写了[一篇文章](http://www.jianshu.com/p/816594c83c74)，写得很详细，帮助大家理解

## 常见问题

- 关于验证码：本项目所用的方法都没有处理验证码，识别复杂验证码的难度就目前来说，还是比较大的。以我的心得来说，做爬虫最好的方式就是尽量规避验证码。
- 代码失效：由于网站策略或者样式改变，导致代码失效，请给我提issue，如果你已经解决，可以提PR，谢谢！

## 其它

- 如果有童鞋自己也实现了某些站点的模拟登陆，可以给我提PR。站点太多了，一个人维护确实是比较大的工作量
- 授人以鱼不如授人以渔，如果感觉自己分析模拟登陆过程还有比较大的困难的，可以仔细阅读一下我写的[这篇文章](http://www.jianshu.com/p/816594c83c74)，通篇基本都是抓包和分析流程
- 如果你有什么比较难登陆的网站，比如发现用了selenium+webdriver都还登陆不了的网站，欢迎给我提issue
- 如果该repo对大家有帮助，给个star鼓励鼓励吧