---
layout: post
title: "如何远程登陆ipython notebook"
description: ""
category: 
tags: []
---
{% include JB/setup %}

#在远程服务器上安装好ipython
##推荐使用EC2

#通过SSH登陆服务器，并利用SSH的本地端口转发功能
##ssh -L *:3001:127.0.0.1:8888 -i ~/Downloads/aws_test.pem ubuntu@ec2-184-72-66-221.compute-1.amazonaws.com
##注意：3001是本地的端口，8888是运行ipython的远程服务器的端口
#登陆服务器后，启动IPYTHON
##ipython notebook --pylab=inline ,则后台会自动启动一个服务：www-browser http://127.0.0.1:8888 
##在本地机器的浏览器中输入:127.0.0.1:3001即可！