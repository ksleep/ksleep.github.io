---
layout: About
title: This is a Title
date: 2021-04-16 19:56:50
tags: 个人日记
type: categories
categories: 
 - 杂谈教程
password: 12345
abstract: Welcome to my blog, enter password to read. 
message: 密码输入框上描述性内容
highlight_shrink: false
description: 这是一段描述文字
---

{% note disabled %}
看到了一个很有趣的Hexo插件，可以轻松实现加密功能
{% endnote %}



今天在浏览大佬的博客时发现了一个挺有趣的Hexo插件功能—-加密Blog。感谢大佬分享😋
下面是添加加密功能的操作：

安装hexo-blog-encrypt插件
在hexo目录下npm install hexo-blog-encrypt
在/Hexo/_config.yml文件中添加内容:

```
encrypt:
	enable:true
```

使用插件
在想要使用加密功能的Blog头部加上对应文字：
YAML

```
---
title: Hexo加密功能
date: 2019-09-04 23:20:00   
tags: [学习笔记,Hexo]
categories: Hexo      
password: smile   
abstract: Welcome to my blog, enter password to read. 
message: 密码输入框上描述性内容
---

```

其中：
password: 该Blog使用的密码
abstract: Blog摘要文字（少量）
message: 密码框上的描述性文字

<div class="btn-center">
{% btn 'https://butterfly.js.org',Butterfly,far fa-hand-point-right,outline larger %}
{% btn 'https://butterfly.js.org',Butterfly,far fa-hand-point-right,outline blue larger %}
{% btn 'https://butterfly.js.org',Butterfly,far fa-hand-point-right,outline pink larger %}
{% btn 'https://butterfly.js.org',Butterfly,far fa-hand-point-right,outline red larger %}
{% btn 'https://butterfly.js.org',Butterfly,far fa-hand-point-right,outline purple larger %}
{% btn 'https://butterfly.js.org',Butterfly,far fa-hand-point-right,outline orange larger %}
{% btn 'https://butterfly.js.org',Butterfly,far fa-hand-point-right,outline green larger %}
</div>


{% note default simple %}
default 提示塊標籤
{% endnote %}

{% note red 'fas fa-bullhorn' simple %}
2021年快到了....
{% endnote %}

{% note blue 'fas fa-bullhorn' disabled %}
2021年快到了....
{% endnote %}

<i style="color:blue;" class="fa fa-bolt fa-2x"></i>

<i style="color:blue;" class="fa fa-bolt fa-spin"></i>



{% note blue 'fa fa-bolt fa-2x' disabled %}
2021年快到了....
{% endnote %}

{% note blue 'iconfont icon-shandian' disabled %}
2021年快到了....
{% endnote %}

1. 带 {% u 下划线 %} 的文本
2. 带 {% emp 着重号 %} 的文本
3. 带 {% wavy 波浪线 %} 的文本
4. 带 {% del 删除线 %} 的文本
5. 键盘样式的文本 {% kbd command %} + {% kbd D %}
6. 密码样式的文本：{% psw 这里没有验证码 %}

- 彩色文字
  在一段话中方便插入各种颜色的标签，包括：{% span red, 红色 %}、{% span yellow, 黄色 %}、{% span green, 绿色 %}、{% span cyan, 青色 %}、{% span blue, 蓝色 %}、{% span gray, 灰色 %}。

- 超大号文字
文档「开始」页面中的标题部分就是超大号文字。
{% span center logo large, Volantis %}
{% span center small, A Wonderful Theme for Hexo %}

{% checkbox 纯文本测试 %}
{% checkbox checked, 支持简单的 [markdown](https://guides.github.com/features/mastering-markdown/) 语法 %}
{% checkbox red, 支持自定义颜色 %}
{% checkbox green checked, 绿色 + 默认选中 %}
{% checkbox yellow checked, 黄色 + 默认选中 %}
{% checkbox cyan checked, 青色 + 默认选中 %}
{% checkbox blue checked, 蓝色 + 默认选中 %}
{% checkbox plus green checked, 增加 %}
{% checkbox minus yellow checked, 减少 %}
{% checkbox times red checked, 叉 %}



{% radio 纯文本测试 %}
{% radio checked, 支持简单的 [markdown](https://guides.github.com/features/mastering-markdown/) 语法 %}
{% radio red, 支持自定义颜色 %}
{% radio green, 绿色 %}
{% radio yellow, 黄色 %}
{% radio cyan, 青色 %}
{% radio blue, 蓝色 %}



{% timeline %}{% timenode 2020-07-24 [2.6.6 -> 3.0](https://github.com/volantis-x/hexo-theme-volantis/releases) %}1. 如果有 `hexo-lazyload-image` 插件，需要删除并重新安装最新版本，设置 `lazyload.isSPA: true`。2. 2.x 版本的 css 和 js 不适用于 3.x 版本，如果使用了 `use_cdn: true` 则需要删除。3. 2.x 版本的 fancybox 标签在 3.x 版本中被重命名为 gallery 。4. 2.x 版本的置顶 `top: true` 改为了 `pin: true`，并且同样适用于 `layout: page` 的页面。5. 如果使用了 `hexo-offline` 插件，建议卸载，3.0 版本默认开启了 pjax 服务。{% endtimenode %}{% timenode 2020-05-15 [2.6.3 -> 2.6.6](https://github.com/volantis-x/hexo-theme-volantis/releases/tag/2.6.6) %}不需要额外处理。{% endtimenode %}{% timenode 2020-04-20 [2.6.2 -> 2.6.3](https://github.com/volantis-x/hexo-theme-volantis/releases/tag/2.6.3) %}1. 全局搜索 `seotitle` 并替换为 `seo_title`。2. group 组件的索引规则有变，使用 group 组件的文章内，`group: group_name` 对应的组件名必须是 `group_name`。2. group 组件的列表名优先显示文章的 `short_title` 其次是 `title`。{% endtimenode %}{% endtimeline %}

这是 {% inlineimage https://cdn.jsdelivr.net/gh/volantis-x/cdn-emoji/aru-l/0000.gif %} 一段话。

这又是 {% inlineimage https://cdn.jsdelivr.net/gh/volantis-x/cdn-emoji/aru-l/5150.gif, height=40px %} 一段话。

{% audio https://github.com/volantis-x/volantis-docs/releases/download/assets/Lumia1020.mp3 %}

# 相册 gallery



`Butterfly` 自带 `gallery` 相册，而且会根据图片大小自动调整排版，效果比 `Volantis` 的 `gallery` 更好，故不再收录 `Volantis` 的 `gallery` 标签。

{% bdage Theme,Butterfly %}
{% bdage Frame,Hexo,hexo %}

{% bdage CDN,JsDelivr,jsDelivr||abcdef,https://metroui.org.ua/index.html,本站使用JsDelivr为静态资源提供CDN加速 %}
//如果是跨顺序省略可选参数，仍然需要写个逗号,用作分割
{% bdage Source,GitHub,GitHub||,https://github.com/ %}

{% bdage Hosted,Vercel,Vercel||brightgreen,https://vercel.com/,本站采用双线部署，默认线路托管于Vercel||style=social&logoWidth=20 %}
//如果是跨顺序省略可选参数组，仍然需要写双竖线||用作分割
{% bdage Hosted,Vercel,Vercel||||style=social&logoWidth=20&logoColor=violet %}

## 网站卡片

{% sitegroup %}
{% site xaoxuu, url=https://xaoxuu.com, screenshot=https://i.loli.net/2020/08/21/VuSwWZ1xAeUHEBC.jpg, avatar=https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/avatar/avatar.png, description=简约风格 %}
{% site inkss, url=https://inkss.cn, screenshot=https://i.loli.net/2020/08/21/Vzbu3i8fXs6Nh5Y.jpg, avatar=https://cdn.jsdelivr.net/gh/inkss/common@master/static/web/avatar.jpg, description=这是一段关于这个网站的描述文字 %}
{% site MHuiG, url=https://blog.mhuig.top, screenshot=https://i.loli.net/2020/08/22/d24zpPlhLYWX6D1.png, avatar=https://cdn.jsdelivr.net/gh/MHuiG/imgbed@master/data/p.png, description=这是一段关于这个网站的描述文字 %}
{% site Colsrch, url=https://colsrch.top, screenshot=https://i.loli.net/2020/08/22/dFRWXm52OVu8qfK.png, avatar=https://cdn.jsdelivr.net/gh/Colsrch/images/Colsrch/avatar.jpg, description=这是一段关于这个网站的描述文字 %}
{% site Linhk1606, url=https://linhk1606.github.io, screenshot=https://i.loli.net/2020/08/21/3PmGLCKicnfow1x.png, avatar=https://i.loli.net/2020/02/09/PN7I5RJfFtA93r2.png, description=这是一段关于这个网站的描述文字 %}
{% endsitegroup %}



<div class="gallery-group-main">
{% galleryGroup MC 在Rikkaの六花服务器里留下的足迹 '/gallery/MC/' https://cdn.jsdelivr.net/gh/Akilarlxh/Picgo@v2.3/tencent/MC/1.jpg %}
{% galleryGroup Gundam 哦咧哇gundam哒！ '/gallery/Gundam/' https://cdn.jsdelivr.net/gh/Akilarlxh/Picgo@v2.3/tencent/Gundam/20200907110508327.png %}
{% galleryGroup I-am-Akilar 某种意义上也算自拍吧 '/gallery/I-am-Akilar/' https://cdn.jsdelivr.net/gh/Akilarlxh/Picgo@v2.3/tencent/I-am-Akilar/20200907113116651.png %}
</div>
```

```

{% folding 查看图片测试 %}

![](https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper/abstract/41F215B9-261F-48B4-80B5-4E86E165259E.jpeg)

{% endfolding %}

{% folding cyan open, 查看默认打开的折叠框 %}

这是一个默认打开的折叠框。

{% endfolding %}

{% folding green, 查看代码测试 %}
假装这里有代码块（代码块没法嵌套代码块）
{% endfolding %}

{% folding yellow, 查看列表测试 %}

- haha
- hehe

{% endfolding %}

{% folding red, 查看嵌套测试 %}

{% folding blue, 查看嵌套测试2 %}

{% folding 查看嵌套测试3 %}

hahaha <span><img src='https://cdn.jsdelivr.net/gh/volantis-x/cdn-emoji/tieba/%E6%BB%91%E7%A8%BD.png' style='height:24px'></span>

{% endfolding %}

{% endfolding %}

{% endfolding %}

# 阿里图标 icon

<i class="iconfont icon-bilibili-fill"></i>

{% icon icon-rat_zi %}{% icon icon-bilibili-fill,4 %}

{% icon icon-rat_zi %}{% icon icon-rat,2 %}

{% icon icon-ox_chou,3 %}{% icon icon-ox,4 %}

{% icon icon-tiger_yin,5 %}{% icon icon-tiger,6 %}

{% icon icon-rabbit_mao,1 %}{% icon icon-rabbit,2 %}

{% icon icon-dragon_chen,3 %}{% icon icon-dragon,4 %}

{% icon icon-snake_si,5 %}{% icon icon-snake,6 %}

{% icon icon-horse_wu %}{% icon icon-horse,2 %}

{% icon icon-goat_wei,3 %}{% icon icon-goat,4 %}

{% icon icon-monkey_shen,5 %}{% icon icon-monkey,6 %}

{% icon icon-rooster_you %}{% icon icon-rooster,2 %}

{% icon icon-dog_xu,3 %}{% icon icon-dog,4 %}

{% icon icon-boar_hai,5 %}{% icon icon-boar,6 %}

```

```