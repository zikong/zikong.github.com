---
layout: post
title:  python标准库:os包和shutil包
date:   2013-05-19 14:50:00
categories: [python]
tags: [python, os, shutil]
---

###os模块

os模块提供了一个统一的操作系统接口函数，os模块能在不同操作系统平台如nt，posix中的特定函数间自动切换，从而实现跨平台操作。

{% highlight python %}
import os

os.getcwd() #获取当前工作目录
os.listdir(path) #获取指定目录下的所有文件和目录 包括隐藏文件
os.chdir(path) #改变当前脚本工作目录到path
os.curdir() #返回当前工作目录

os.mkdir(path) #创建目录
os.rmdir(path) #删除空目录，若目录不为空则无法删除
os.pardir() #获取当前目录的父目录路径
os.remove() #删除一个文件
os.rename(path1 ,path2) #重命名文件

os.chmod(path ,mode) #改变文件权限模式
os.access(path ,mode) #检验文件权限模式

os.sep    #输出操作系统特定的路径分隔符。win下为"\\",macx下为"/"
os.linesep    #输出当前平台使用的行终止符
os.pathsep    #输出用于分割文件路径的字符串
os.name    #输出字符串指示当前使用平台。win->'nt'; mac->'posix'
os.system(command) #运行shell命令
os.environ #获取系统环境变量
{% endhighlight %}

###shutil模块
{% highlight python %}
import shutil

copy(src ,dst) #复制文件，从src到dst
move(src ,dst) #移动文件，从src到dst
{% endhighlight %}