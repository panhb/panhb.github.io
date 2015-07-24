---
layout:     post
title:      Docker学习笔记（一）
subtitle:   学习使用docker构建项目
date:       2015-07-24 23:00:00
author:     Panhb
header-img: "img/post-bg-008.jpg"
tags: docker
---

最近在学习使用docker构建项目，原理神马的，我也将不清楚，只是做我个人学习的一个记载。   

由于我是win用户，搭docker的环境，自然麻烦多多。首先就是安装Boot2Docker，基本上也就是一直下一步的节奏。但是start虚拟机的时候，可能会窗口可能会闪一下。我的原因是我的电脑的CPU虚拟机支持没有开启，只需在BIOS里面设置一下即可
```javascript        
Configuratio > Intel Virtual Technology > Enabled
``` 

然后daocloud提供镜像加速，win下面命令如下
```javascript              
boot2docker up               
boot2docker ssh "echo $'EXTRA_ARGS=\"--registry-mirror=http://8e3b4e3c.m.daocloud.io\"' | sudo tee -a /var/lib/boot2docker/profile && sudo /etc/init.d/docker restart"
```   

然而我正在使用是docker云，并没有在本地构建环境跑，蛤蛤   

我了解到的国内的docker云有三家，时速云、daocloud和灵雀云。使用过时速云和daocloud，不敢从深层次的方向去对比这两个云，只能就我使用的感受，时速云给我体验很差，用过三次，两次他们家服务器宕机。创建的应用那二级域名也是醉，不忍直视。目前使用的是daocloud，docker搭建的整体结构很清晰，更容易上手，交互也不错，还支持coding的对接，想想github+daocloud，完美替代coding的演示功能。唯一不好的就是可创建的服务实例太！少！了！完全不够用好么，还有容器。免费用户我就不叨叨了，毕竟人家还要靠这个赚钱钱。      


不过docker云唯一不好的缺点是，我在云上看不到具体构建的镜像代码，必须去github上看，感觉好麻烦。既然已经从github那clone过来了，为毛线不再搞个看代码的地方咧，不晓得以后会不会改进，获取我提的这个需求，没啥意义，好吧，我果然是个蛋疼的汉纸，蛤蛤。   


###最后附上   [**Daocloud**](https://www.daocloud.io)   