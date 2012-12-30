---
layout: post
title: "如何远程登陆ipython notebook"
description: ""
category: 
tags: []
---
{% include JB/setup %}

##在远程服务器上安装好ipython
  推荐使用EC2

##通过SSH登陆服务器，并利用SSH的本地端口转发功能
~~~~~

ssh -L *:3001:127.0.0.1:8888 -i ~/Downloads/aws_test.pem ubuntu@ec2-184-72-66-221.compute-1.amazonaws.com

~~~~~

注意：3001是本地的端口，8888是运行ipython的远程服务器的端口

##登陆服务器后，启动IPYTHON
~~~~~

ipython notebook --pylab=inline 

~~~~~

上述命令运行后，ipython会在后台自动启动一个服务：www-browser http://127.0.0.1:8888 

##在本地机器的浏览器中输入:127.0.0.1:3001即可！

>关于SH的介绍可参考[这里](http://zh.wikipedia.org/wiki/SSH),[这里](http://www.ruanyifeng.com/blog/2011/12/ssh_remote_login.html),[这里](http://www.ruanyifeng.com/blog/2011/12/ssh_port_forwarding.html)和[这里](http://www.ibm.com/developerworks/cn/linux/l-cn-sshforward/)