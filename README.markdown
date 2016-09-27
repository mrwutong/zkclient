ZkClient: a zookeeper client, that makes life a little easier.
=====

+ 关于原版README: 请参照[README.ORIGIN][]
+ 感谢Jimmy.Yang的分享，来自链接[dubbox升级spring到4.x及添加log4j2支持](http://www.cnblogs.com/yjmyzz/p/update-dubbo-to-spring-4-and-add-log4j2-support.html)
+ 改版README的目的是想把发布的过程记录一下

Build ZkClient from sources:
---------------

+ 安装groovy及gradle
+ git clone https://github.com/mrwutong/zkclient.git
+ 因oschina的repository有时无法访问，编译时一直停止在:compile阶段
+ 注释掉`build.gradle`的23~26行（我已经注释），知道就好
+ 进行编译`gradle jar`（不是官方的`./gradlew jars`），我的系统是MACOS

Howto release ZkClient as local repository
---------------

+ 将上步编译好的jar包`zkclient-0.8.1.jar`找到，一般路径为`<工程>/build/libs/zkclient-0.8.1.jar`
+ 运行maven命令安装到本地repository（如想发布至私服上请自己搜一下网上很多）

```shell
mvn install:install-file -Dfile=<zkclient工程路径>/build/libs/zkclient-0.8.1.jar -DgroupId=com.101tec -DartifactId=zkclient -Dversion=0.8.1 -Dpackaging=jar
```

*注* 请将上面<zkclient工程路径>替换为你的路径
