# linux 下百度云盘下载器

## install aria2

`sudo apt-get install aria2`

`mkdir ~/.aria2 #新建文件夹用来放置软件配置文件`

`sudo touch ~/.aria2/aria2.session #新建session文件 `

`cp ./aria2.conf.example ~/.aria2/aria2.conf #将文件夹下配置模板复制到刚才新建的文件夹` 

**注意：** 下载器的默认下载路径在aria2.conf 中指定，除在配置文件中，其他位置无法更改下载路径

### 运行方法

`aria2c --conf-path=/home/xxx/文档/aria2/aria2.conf [-D] #可选项参数-D后台执行`

如无特殊需求，程序服务器执行后占用6800端口，若已经被占用可在之前提到的配置文件中进行更改

## 配置Chrome 百度云下载插件

项目地址：https://github.com/acgotaku/BaiduExporter.git

将文件夹下BaiduExporter里的Chrome插件加入Chrome扩展程序中

安装完成后，每次打开百度云后,会在页面上多一个 **导出下载** 标签，选择标签下菜单中第一个选项，自动加载进aria2下载器的下载列表中进行下载，若出现问题可以选择第二个选项，会导出下载链接，然后单独在shell下执行aria2下载命令。设置中貌似可以更改下载路径，未做尝试。

下载测试：https://pan.baidu.com/s/17p0gzG-wCA4QfRgdfuHuyw

正常情况下会在运行Aria2服务器的terminal下显示下载信息。

##配置aria2下载器前端

为了使文件下载信息便于显示，可以配置一个Web前端进行监控。

项目地址：http://ariang.mayswind.net/zh_Hans/

aria2没有官方GUI，不过有多个第三方webGui, 目前试用情况下感觉都有不足之处，上面给出的是较新的一个第三方前端，可以尝试一下，不过我并没有进行过使用，如有问题烦请Google。

## 结语

Aria2是Linux下非常强大的下载工具，不足之处就是没有较完善的前端GUI，有一定学习门槛，它不止可以下载百度云文件，例如迅雷等磁力链接文件都可以用Aria2进行下载。具体更为高级的使用方法，参考下面给出链接：
1.https://www.jianshu.com/p/b2649d073741

2.https://aria2.github.io/