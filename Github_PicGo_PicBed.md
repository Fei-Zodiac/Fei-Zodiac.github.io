# Github + PicGo 图床搭建
## 背景
平时我们在知识学习的过程中，大部分人或多或少都会去写相关的文档来记录和梳理知识。诸如Microsoft 的Word，OneNote这样的编辑器，由于受限于Window平台的原因，当我们想要把本地的知识通过网络分享到网站上时，往往都需要对文档进行重新编排来适应网站的格式，在这其中必然要需要花费大量的编辑时间，而这个时候Markdown是个很不错的选择。Markdown是一个与平台无关的轻量级文本标记语言，语法相当简单，只需要支持Markdown的文本应用就能打开并查看格式化后的文档，而且现在越来越多的网站也开始或已经支持Markdown,这已经成为一种趋势。

关于Markdown的优势在这里就不再赘述，有兴趣的可以看看关于Markdown的语法篇。那么在编辑文档时候，我们往往会用到一些图片信息。特别是在写教程的时候，图文并茂的文档更容易让人接受和理解，读起来也赏心悦目、有趣些，缓解了纯文本那种苦涩。那么问题来了，插入的图片路径如果是本地的，那么文档换个机器或者哪怕是换个路径，也就不能正确找到原来的图片了。


## PicGo
### 简介
PicGo Github 项目地址:  <https://github.com/Molunerfinn/PicGo>.
根据官方的描述，PicGo是一个用于快速上传图片并获取图片 URL 链接的工具，PicGo 工具本身可以支持很多种服务器，如下：

+ 七牛图床 v1.0
+ 腾讯云 COS v4\v5 版本 v1.1 & v1.5.0
+ 又拍云 v1.2.0
+ GitHub v1.5.0
+ SM.MS V2 v2.3.0-beta.0
+ 阿里云 OSS v1.6.0
+ Imgur v1.6.0

作为个人用户，免费的Githu是个不错的选择，一来省去了麻烦地配置云服务器，二来还可以省掉服务器租赁费用。所以对于没有云服务器硬件的Markdown用户，Github可谓是首选。

### 特色功能
+ 支持拖拽图片上传
+ 支持快捷键上传剪贴板里第一张图片
+ Windows 和 macOS 支持右键图片文件通过菜单上传 (v2.1.0+)
+ 上传图片后自动复制链接到剪贴板
+ 支持自定义复制到剪贴板的链接格式
+ 支持修改快捷键，默认快速上传快捷键：command+shift+p（macOS）| control+shift+p（Windows\Linux)
+ 支持插件系统，已有插件支持 Gitee、青云等第三方图床
+ 支持通过发送 HTTP 请求调用 PicGo 上传（v2.2.0+)

### 下载安装
各平台安装包[下载地址](https://github.com/Molunerfinn/PicGo/releases)，其中还提供了源码包。
#### Windows
Windows 用户推荐下载最新版本的 exe 文件

#### MacOS
MacOS  用户推荐下载最新版本的 dmg 文件。

还可以使用 brew cask 来安装 PicGo: brew cask install picgo

#### Linux
Linux用户推荐下载 AppImage 文件。

更多的安装方式请参考官方文档<https://github.com/Molunerfinn/PicGo>，本文以MacOS平台例子作为演示。

安装完成后应用界面如下：

![PicGo](https://raw.githubusercontent.com/Molunerfinn/test/master/picgo/picgo-2.0.gif)
_____________________
![PicGo](https://user-images.githubusercontent.com/12621342/34242310-b5056510-e655-11e7-8568-60ffd4f71910.gif)
_____________________



## Github 搭建
1. **新建一个repository**
![](https://i.loli.net/2020/09/19/RzBt13Xuh4LOJy5.png)
_____________________
2. **生成新的token**
点击**账户头像->Setting**
![](https://i.loli.net/2020/09/19/2burWzTKt159PA6.png)
_____________________
选择**Development settings**
![](https://i.loli.net/2020/09/19/6avJk3HV9pwqL1n.png)
_____________________
选择**Personal access tokens->Generate new token->复制token值**
![](https://i.loli.net/2020/09/19/EY13OiN5y6xuzn4.png)
_____________________
勾选**repo->Generate token**
![](https://i.loli.net/2020/09/19/FjKwgXQyTGCcob3.png)
_____________________
![](https://i.loli.net/2020/09/19/ZiWoLUC1Rl28D7A.png)
_____________________

3. 配置PicGo
    填入刚创建的repository名字，分值为master,toke为上一步复制的token值。


**这里没有配置成功，不知道是哪里出了错，PicGo每次都是上传到SM.MS网站上去。后续还需要仔细检查可能错在哪里**
    ![](https://i.loli.net/2020/09/19/YLUXTxQmJlIV92K.png)

