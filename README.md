Pure CSS 中文网站
=================

这是[Pure CSS][pure]的展示网站（中文版）


[pure]: https://github.com/yui/pure


本地运行
--------

这是一个基于node.js的网站，使用了Express.js，这意味着，在本地可以很容易跑起来（前提是你要先安装了node.js）

```shell
$ npm i
$ node server
```

### 和Pure一起在本地运行

当你对[`pure`][pure]做了本地的改变后，你就可以通过这个网站验证下变化。接下来几步是要解释这个网站怎么和Pure一起运行，首先，你要确定你已经安装了[Bower][](如果没安装，请执行以下命令: `sudo npm -g i bower`)，其次，进入到本地的`pure`目录，通过`grunt`构建，然后用Bower创建一个全局的链接:

```shell
$ cd pure
$ npm i #第一次需要安装依赖
$ bower install #第一次需要安装bower组件
$ grunt
$ bower link
```

现在进入Pure-site的目录，如果还没有安装依赖，请先`npm i`一下，然后在`pure-site`中用Bower去链接`pure`，最后启动服务器：

```shell
$ cd ../pure-site
$ npm i
$ bower link pure
$ node server --pure-local
```

这个 `--pure-local` 参数表明这个网站将使用本地的Pure，而不是用CDN上的Pure

**注意：** 在你启动服务器的时候，安装包依赖（npm install）和用Bower去链接pure这两步操作，*不需要*每次都做。当然，你需要保持服务器一直在运行着，并且用`grunt`去重建`pure`，然后在浏览器刷新，你才能看到Pure的改变。


[Bower]: http://bower.io/


LICENSE
-------

这个软件在Yahoo的BSD许可证下，可免费使用。
查看 [LICENSE file][] 的许可证信息和版权信息

[LICENSE file]: https://github.com/yui/pure-site/blob/master/LICENSE.md
