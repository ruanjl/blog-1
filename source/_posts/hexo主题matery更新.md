title: hexo主题matery更新
date: 2018-10-04 12:47:58
tags: [hexo主题]
categories: [综合]
---
### 修改社交链接
在主题文件的layout/_partial/social-link.ejs文件中，你可以找到social-link的内容，可以在其中添加你需要的链接地址，增加内容如：
```java
<a href="https://github.com/ciweigg2" class="tooltipped" target="_blank" data-tooltip="访问我的GitHub" data-position="top" data-delay="50">
    <i class="fa fa-github"></i>
</a>
<a href="#" class="tooltipped" target="_blank" data-tooltip="邮件联系我" data-position="top" data-delay="50">
    <i class="fa fa-envelope-open"></i>
</a>
<a href="#!" class="tooltipped" data-tooltip="QQ联系我:"#" data-position="top" data-delay="50">
    <i class="fa fa-qq"></i>
</a>
<% if (config.feed && config.feed.path == 'atom.xml') { %>
<a href="<%- url_for('/atom.xml') %>" class="tooltipped" target="_blank" data-tooltip="RSS 订阅" data-position="top" data-delay="50">
    <i class="fa fa-rss"></i>
</a>
<% } %>
```

<!--more-->

### 修改主题颜色
在主题文件的/source/css/matery.css文件中，搜索.bg-color来修改背景颜色：
```java
修改第一个背景颜色
body {
    background-color: #ffffff;
    margin: 0;
    color: #34495e;
}

修改第二个标题栏颜色 .bg-color
.bg-color {
    background-color: #139ab6 !important;
}

注释掉下面2个颜色切换的
/*
@-webkit-keyframes rainbow {
   /* 动态切换背景颜色. */
}

@keyframes rainbow {
    /* 动态切换背景颜色. */
}
*/
```

### 修改banner图和文章特色图
```java
/layout/_partial/bg-cover.ejs
修改背景图
$('.bg-cover').css('background-image', 'url(http://ciwei2.ufile.ucloud.com.cn/' + new Date().getDay() + '.jpg)');
```

### 主题_config.yml中的gitalk配置

```java
gitalk:
  enable: true
  owner: ciweigg2
  repo: ciweigg2.github.io
  oauth:
    clientId: 4e9a7bfed30119302290
    clientSecret: 28f6acd9ebbeff567a56b52da427a6622f861607
  admin:
    - ciweigg2
```

### 修改文章随机图片和内容
```java
_config.yml

添加菜单呀
menu:
  首页:
    url: /
    icon: fa-home
  博客:
    url: /Home
    icon: fa-home
  前端:
    url: /GuideV2/FrontEndGuide
    icon: fa-archive
  生活:
    url: /garlly
    icon: fa-bicycle
  标签:
    url: /tags
    icon: fa-tags
  分类:
    url: /categories
    icon: fa-bookmark
  归档:
    url: /archives
    icon: fa-archive
  关于:
    url: /about
    icon: fa-user-circle-o    

修改内容呀
dream:
  enable: true
  text: 要用多少个晴天 交换多少张相片 还记得锁在抽屉里面的滴滴点点 小而温馨的空间 因为有你在身边
修改文章的随机图片
featureImages: 
- http://ciwei2.ufile.ucloud.com.cn/0.jpg
- http://ciwei2.ufile.ucloud.com.cn/1.jpg
- http://ciwei2.ufile.ucloud.com.cn/2.jpg
- http://ciwei2.ufile.ucloud.com.cn/3.jpg
- http://ciwei2.ufile.ucloud.com.cn/4.jpg
- http://ciwei2.ufile.ucloud.com.cn/5.jpg
- http://ciwei2.ufile.ucloud.com.cn/6.jpg
- http://ciwei2.ufile.ucloud.com.cn/7.jpg
- http://ciwei2.ufile.ucloud.com.cn/8.jpg
- http://ciwei2.ufile.ucloud.com.cn/9.jpg
- http://ciwei2.ufile.ucloud.com.cn/10.jpg
- http://ciwei2.ufile.ucloud.com.cn/11.jpg
- http://ciwei2.ufile.ucloud.com.cn/12.jpg
- http://ciwei2.ufile.ucloud.com.cn/13.jpg
- http://ciwei2.ufile.ucloud.com.cn/14.jpg
- http://ciwei2.ufile.ucloud.com.cn/15.jpg
- http://ciwei2.ufile.ucloud.com.cn/16.jpg
- http://ciwei2.ufile.ucloud.com.cn/17.jpg
- http://ciwei2.ufile.ucloud.com.cn/18.jpg
- http://ciwei2.ufile.ucloud.com.cn/19.jpg
- http://ciwei2.ufile.ucloud.com.cn/20.jpg
- http://ciwei2.ufile.ucloud.com.cn/21.jpg
- http://ciwei2.ufile.ucloud.com.cn/22.jpg
- http://ciwei2.ufile.ucloud.com.cn/23.jpg
- http://ciwei2.ufile.ucloud.com.cn/24.jpg
- http://ciwei2.ufile.ucloud.com.cn/25.jpg
- http://ciwei2.ufile.ucloud.com.cn/26.jpg
- http://ciwei2.ufile.ucloud.com.cn/27.jpg
- http://ciwei2.ufile.ucloud.com.cn/28.jpg
- http://ciwei2.ufile.ucloud.com.cn/29.jpg
- http://ciwei2.ufile.ucloud.com.cn/30.jpg
- http://ciwei2.ufile.ucloud.com.cn/31.jpg
- http://ciwei2.ufile.ucloud.com.cn/32.jpg
- http://ciwei2.ufile.ucloud.com.cn/33.jpg
- http://ciwei2.ufile.ucloud.com.cn/34.jpg
- http://ciwei2.ufile.ucloud.com.cn/35.jpg
- http://ciwei2.ufile.ucloud.com.cn/36.jpg
- http://ciwei2.ufile.ucloud.com.cn/37.jpg
- http://ciwei2.ufile.ucloud.com.cn/38.jpg
- http://ciwei2.ufile.ucloud.com.cn/39.jpg
- http://ciwei2.ufile.ucloud.com.cn/40.jpg
- http://ciwei2.ufile.ucloud.com.cn/41.jpg
- http://ciwei2.ufile.ucloud.com.cn/42.jpg
- http://ciwei2.ufile.ucloud.com.cn/43.jpg
- http://ciwei2.ufile.ucloud.com.cn/44.jpg
- http://ciwei2.ufile.ucloud.com.cn/45.jpg
- http://ciwei2.ufile.ucloud.com.cn/46.jpg
- http://ciwei2.ufile.ucloud.com.cn/47.jpg
- http://ciwei2.ufile.ucloud.com.cn/48.jpg
- http://ciwei2.ufile.ucloud.com.cn/49.jpg
- http://ciwei2.ufile.ucloud.com.cn/50.jpg
- http://ciwei2.ufile.ucloud.com.cn/51.jpg
- http://ciwei2.ufile.ucloud.com.cn/52.jpg
- http://ciwei2.ufile.ucloud.com.cn/53.jpg
- http://ciwei2.ufile.ucloud.com.cn/54.jpg
- http://ciwei2.ufile.ucloud.com.cn/55.jpg
- http://ciwei2.ufile.ucloud.com.cn/56.jpg
- http://ciwei2.ufile.ucloud.com.cn/57.jpg
- http://ciwei2.ufile.ucloud.com.cn/58.jpg
- http://ciwei2.ufile.ucloud.com.cn/59.jpg
- http://ciwei2.ufile.ucloud.com.cn/60.jpg
- http://ciwei2.ufile.ucloud.com.cn/61.jpg
- http://ciwei2.ufile.ucloud.com.cn/62.jpg
- http://ciwei2.ufile.ucloud.com.cn/63.jpg
- http://ciwei2.ufile.ucloud.com.cn/64.jpg
- http://ciwei2.ufile.ucloud.com.cn/65.jpg
- http://ciwei2.ufile.ucloud.com.cn/66.jpg
- http://ciwei2.ufile.ucloud.com.cn/67.jpg
- http://ciwei2.ufile.ucloud.com.cn/68.jpg
- http://ciwei2.ufile.ucloud.com.cn/69.jpg
- http://ciwei2.ufile.ucloud.com.cn/70.jpg
- http://ciwei2.ufile.ucloud.com.cn/71.jpg
- http://ciwei2.ufile.ucloud.com.cn/72.jpg
- http://ciwei2.ufile.ucloud.com.cn/73.jpg
- http://ciwei2.ufile.ucloud.com.cn/74.jpg
- http://ciwei2.ufile.ucloud.com.cn/75.jpg
- http://ciwei2.ufile.ucloud.com.cn/76.jpg
- http://ciwei2.ufile.ucloud.com.cn/77.jpg
- http://ciwei2.ufile.ucloud.com.cn/78.jpg
- http://ciwei2.ufile.ucloud.com.cn/79.jpg
- http://ciwei2.ufile.ucloud.com.cn/80.jpg
- http://ciwei2.ufile.ucloud.com.cn/81.jpg
- http://ciwei2.ufile.ucloud.com.cn/82.jpg
- http://ciwei2.ufile.ucloud.com.cn/83.jpg
- http://ciwei2.ufile.ucloud.com.cn/84.jpg
- http://ciwei2.ufile.ucloud.com.cn/85.jpg
- http://ciwei2.ufile.ucloud.com.cn/86.jpg
- http://ciwei2.ufile.ucloud.com.cn/87.jpg
- http://ciwei2.ufile.ucloud.com.cn/88.jpg
- http://ciwei2.ufile.ucloud.com.cn/89.jpg
- http://ciwei2.ufile.ucloud.com.cn/90.jpg
- http://ciwei2.ufile.ucloud.com.cn/91.jpg
- http://ciwei2.ufile.ucloud.com.cn/92.jpg
- http://ciwei2.ufile.ucloud.com.cn/93.jpg
- http://ciwei2.ufile.ucloud.com.cn/94.jpg
- http://ciwei2.ufile.ucloud.com.cn/95.jpg
- http://ciwei2.ufile.ucloud.com.cn/96.jpg
- http://ciwei2.ufile.ucloud.com.cn/97.jpg
- http://ciwei2.ufile.ucloud.com.cn/98.jpg
- http://ciwei2.ufile.ucloud.com.cn/99.jpg
- http://ciwei2.ufile.ucloud.com.cn/100.jpg
- http://ciwei2.ufile.ucloud.com.cn/101.jpg
- http://ciwei2.ufile.ucloud.com.cn/102.jpg
- http://ciwei2.ufile.ucloud.com.cn/103.jpg
- http://ciwei2.ufile.ucloud.com.cn/104.jpg
- http://ciwei2.ufile.ucloud.com.cn/105.jpg
- http://ciwei2.ufile.ucloud.com.cn/106.jpg
- http://ciwei2.ufile.ucloud.com.cn/107.jpg
- http://ciwei2.ufile.ucloud.com.cn/108.jpg
- http://ciwei2.ufile.ucloud.com.cn/109.jpg
- http://ciwei2.ufile.ucloud.com.cn/110.jpg
- http://ciwei2.ufile.ucloud.com.cn/111.jpg
- http://ciwei2.ufile.ucloud.com.cn/112.jpg
- http://ciwei2.ufile.ucloud.com.cn/113.jpg
- http://ciwei2.ufile.ucloud.com.cn/114.jpg
- http://ciwei2.ufile.ucloud.com.cn/115.jpg
- http://ciwei2.ufile.ucloud.com.cn/116.jpg
- http://ciwei2.ufile.ucloud.com.cn/117.jpg
- http://ciwei2.ufile.ucloud.com.cn/118.jpg
- http://ciwei2.ufile.ucloud.com.cn/119.jpg
- http://ciwei2.ufile.ucloud.com.cn/120.jpg
- http://ciwei2.ufile.ucloud.com.cn/121.jpg
- http://ciwei2.ufile.ucloud.com.cn/122.jpg
- http://ciwei2.ufile.ucloud.com.cn/123.jpg
- http://ciwei2.ufile.ucloud.com.cn/124.jpg
- http://ciwei2.ufile.ucloud.com.cn/125.jpg
```