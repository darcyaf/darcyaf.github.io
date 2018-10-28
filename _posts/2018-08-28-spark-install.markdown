---
title:  "Spark系列"
subtitle: "安装时问题"
author: "darcyaf"
avatar: "img/authors/darcyaf.jpeg"
image: "img/2018-10-27_diaochan.jpeg"
date:   2018-10-28 23:00:12
---

# Spark环境搭建

## 安装Spark

- [官网地址](http://apache.claz.org/spark/spark-2.3.2/spark-2.3.2-bin-hadoop2.7.tgz)下载`Spark`的压缩包
- 解压Spark文件到`/usr/local`目录，命令为：
```sh
    sudo tar zxvf spark-2.3.2-bin-hadoop2.7.tgz -C /usr/local 
```
-  至此`Spark`已经安装完成，为方便使用，先可以做一个软连接：

```sh
    sudo ln -s /usr/local/spark-2.3.2-bin-hadoop2.7 /usr/local/spark
```
在.zshrc中修改`PATH`,将Spark 的bin目录放入PATH当中:
```sh
    export SPARK_HOME=/usr/local/spark
    export PATH=$PATH:$SPARK_HOME/bin:$SPARK_HOME/sbin
```
最后`source ~/.zshrc`就可以使配置生效了