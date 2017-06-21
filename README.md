自从上次写了《Android检查版本升级应该怎么做？》
```
简书文章地址：http://www.jianshu.com/p/98ea7e866ffd
```
后，有很多同学让我提供一份demo。所以就有了UpgradeDemo演示是如何做的检查版本升级。

接下来做一些代码说明
##upgrade包
存放核心的检查升级代码、`DownloadManager`下载apk文件等。具体大家详细看，有什么不明白的与我交流沟通吧。

##Constants类
####定义了两个变量
-`API_DOMAIN_DEBUG`是测试服务器基地址，如http://rapapi.org/mockjs/21104
-`API_DOMAIN_RELEASE`是正式服务器基地址，大家根据自己的实际情况填写吧。

##ApiCommonRequest类
upgrade方法用于从服务器端请求最新版本的信息。

##注意
demo使用的是`gradle`版本是3.3，`targetSdkVersion`是25，如果运行在系统版本在6.0及以上，记得适配权限。