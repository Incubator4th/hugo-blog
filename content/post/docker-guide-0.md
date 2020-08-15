---
title: "Docker从零入门 0 前言和简介"
date: 2020-08-15T19:47:28+08:00
tags:
  - docker
categories:
  - docker
---
![docker-log](/image/docker/logo.png)

## 前言

### 关于读者

没有任何要求，基本上在会使用命令行(cmd和powershell也是)的前提下即刻

拖了很久的《Docker从零入门到~~精通~~使用》 终于迈出了第零步  

依照惯例，数组下标都是从零开始的，这个系列也不意外。写在正文之前，是想简单的和大家聊一聊Docker整个技术以及我的见解，正文的使用可以从第一篇开始看。

---

## 接触Docker

第一次接触到Docker这个单词，是在大学的系统架构入门课上。当时的教授和我们聊了一些关于Docker的相关概念，比如方便部署容易打包等等。但是在那个时候我对Docker的概念还比较模糊，由于早前接触过Linux上的AppImage，它是属于一个应用程序的封包，使得不同的发行版Linux能够直接安装使用而不用特地找deb/rpm包等等。

最开始Docker给我的概念就是这样，也许是我没有仔细研究，也许是教授没有讲的很详细，当在解释应用部署等等的时候，提到可以用Docker的时候，总是误以为是一个二进制封包而已，而AppImage伴随着的可能是过旧的系统版本和违背Linux理念难以修改的应用本体和配置文件等等。


## 使用Docker

刚开始使用Docker是在刚刚工作的时候，其实也不远，因为距离至今也只过去了一年多一些时间。

在公司上有业务上的需求，简单的介绍一下，公司的业务在CTF(网络安全夺旗竞赛)上需要做到每个人独立的环境和隔离的应用。在选型中，属于新兴事物的Docker有着无与伦比的契合性，无论是独立每个用户的使用空间上，还是在随用随释放的资源上，以及更方便的维护破坏性修改，也算是赶鸭子上架研究Docker技术了。


## Docker简介

简单的说了些我自己的事情，我们的正头戏还是为了讲一下Docker的使用。在运维部署方面，Docker，应该说容器技术，在虚拟机技术之后发展，比起虚拟机通过模拟出虚拟的硬件来提供独立的环境而言。Docker容器技术通过linux的特有技术namespace命名空间的隔离，来使得容器能实现类似于虚拟机一样的隔离环境，但是在镜像的大小和启动的速度而言相比虚拟机技术提升了很大的档次。

### Docker的不同版本

在docker的官网和社区上，可以找到不同的版本，诸如面向社区的CE版，面向企业的EE版，以及面向早期社区的io版本。

本质上，不同的版本在后续的教程上没有大多的差别，为了保险起见，一般使用的都是docker-ce 19.03的版本，使用 1.40版本的API

### Docker 相关概念

docker最核心的理念中，分为两部分——镜像和容器，借用官方的例子来说。

镜像是通过制作得出的可以迁移和复制的实体，可以类比 OOP概念中的Class类和二进制文件

容器是通过镜像运行而创建的动态服务资源，可以类比为 对象 和 进程

关于Docker技术的入门，就围绕着这两个核心部分来介绍，从学会使用官方容器，到制作属于自己的镜像。
