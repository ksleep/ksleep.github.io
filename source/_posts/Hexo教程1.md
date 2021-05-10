---
title: Hexo+GitHub+Netlify一站式部署
date: 2021-04-27 15:27:24
tags: Hexo
type: categories
categories: 
 - Hexo部署教程
sticky: 1
description: github + netlify 部署
cover: http://ghostmask.gitee.io/myimg/Myimg/shanhaizy/25.jpg
---


{% span center logo large, Hexo+GitHub+Netlify一站式搭建属于自己的博客网站%}



{% icon icon-1_round_solid,2 %}{% del 基于码云部署hexo %} 

由于码云pages 基于本家的域名部署需要收费，且每次push代码之后都需要重新部署，故放弃

<br>

{% icon icon-2_round_solid,2 %}{% del 基于coding部署hexo %} 

**公测期，免费用：**新版 CODING Pages 网站托管服务现已正式公测，公测期间，静态或动态网站均可体验免费部署 由于coding在短信通知下，2021.5.30日会下线就就网站部署方式，而新网站部署看起来过于麻烦，故放弃

<br>

{% icon icon-3_round_solid,2 %}{% del 基于github pages部署hexo %} 

<br>

放弃原因：

 <li>&nbsp;&nbsp;&nbsp;1. github pages 虽然能和相关域名解析关联，但githubs偶尔会导致自动生成的https证书无法正常使用 </li>  

<li>&nbsp;&nbsp;&nbsp;2. github虽然没有被墙，但那个访问速度偶尔会非常的慢，及其不稳定 </li> 

<li>&nbsp;&nbsp;&nbsp;3. 百度无法抓取</li>  

<li>&nbsp;&nbsp;&nbsp;4. 无法做CDN加速</li>  

 故放弃github pages的方案

<br>

## 部署

最后采用github管理源代码，Netlify自动部署的方式[Netlify](https://www.netlify.com/)`https://www.netlify.com/`的官网，然后点击右上角Sign up注册账号，选择GitHub关联登录。

![image-20210507150017073](https://gitee.com/GhostMask/Myimg/raw/master/img/image-20210507150017073.png)

注册后点击创建新站点，选择GitHub会有提示框进行认证

![image-20210507151448439](https://gitee.com/GhostMask/Myimg/raw/master/img/image-20210507151448439.png)

选择上传到远程仓库的hexo项目文件，然后进行关联

![image-20210507151610929](https://gitee.com/GhostMask/Myimg/raw/master/img/image-20210507151610929.png)

最后按照步骤发布，点击deploy site 等待就可以了

![image-20210507151737671](https://gitee.com/GhostMask/Myimg/raw/master/img/image-20210507151737671.png)

部署成功后即可生成一个带有netlify的域名，这时候访问这个自动生成的域名就可以看到一个属于自己的博客网站了。但我们要的是把自己的域名解析，

##  域名解析

 域名管理里面添加两条解析记录，一条A记录，一条CNAME记录，对于的值即是netlify网站给你的博客自动生成的域名值，这样添加之后就能将你的域名绑定到netlify了

![image-20210507152624169](https://gitee.com/GhostMask/Myimg/raw/master/img/image-20210507152624169.png)

域名绑定

第二步

![image-20210507152907599](https://gitee.com/GhostMask/Myimg/raw/master/img/image-20210507152907599.png)

输入域名后进行添加

![image-20210507153229898](https://gitee.com/GhostMask/Myimg/raw/master/img/image-20210507153229898.png)

添加之后可以发现 ，域名已经完全解析成功

![image-20210507153315012](https://gitee.com/GhostMask/Myimg/raw/master/img/image-20210507153315012.png)

这个时候输入xxx.cn 你的域名就能成功访问到属于自己的博客网站了

## 添加HTTPS

因为`Netlify` 自带 `Let’s Encrypt Certificate.`的免费证书，所以如果没有ssl证书的话可以直接用`Netlify`自带的证书。

如果想用自己的ssl证书，下载自己的证书后会看到证书里有一个Apache的文件夹，里面有三个文件，结构如下：

```
1_root_bundle.crt
2_hhwen.cn.crt
3_hhwen.cn.key
```

按照如下图方式复制保存

![image-20210507154316287](https://gitee.com/GhostMask/Myimg/raw/master/img/image-20210507154316287.png)