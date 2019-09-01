flume学习笔记

什么是flume？ 网上自查定义与介绍

flume能够通过执行shell命令进行日志的采集，或者是监控指定目录下文件的变动来实现同步式的采集，其下三个模块source sink channel分别对应着接受、发送和中转三个功能，其中中转能够进行一些简单的数据处理比如封装打包或者是给数据添加标签用来方便后续的分类处理。<a href="http://blog.csdn.net/ty4315/article/details/53243769">三个模块不同种类的介绍。</a>

在这几天的学习和使用中，我接触到的是flume在docker容器中搜集cpu使用率以及内存使用情况的日志，发送到kafka中，然后进行相应的持久化操作。具体的方式就是使用exec source执行iostats -c 1 命令（只有cpu），然后发送到kafka相应的topic中。

这么做主要是考虑到弹性调度中可能会需要使用到这些度量值。