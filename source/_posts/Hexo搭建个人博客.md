---
title: Hexo搭建个人博客
date: 2019-06-17 22:52:07
tags:
	- 导航
	- 分享
categories: Hexo
---


# Hexo配置

## 软件安装
软件安装请参考Hexo官方安装教程。
[Hexo安装](https://hexo.io/zh-cn/docs/)

## 软件配置
软件配置请参考Hexo官方建站教程。
[Hexo建站](https://hexo.io/zh-cn/docs/setup)	

# 主题
## 下载主题
本文采用NEXT主题为例。
在终端窗口下，定位到 Hexo 站点目录下。使用 Git checkout 代码：
```
$ cd your-hexo-site
$ git clone https://github.com/iissnan/hexo-theme-next themes/next
```
## 启用主题
与所有 Hexo 主题启用的模式一样。 当 克隆/下载 完成后，打开 站点配置文件， 找到 theme 字段，并将其值更改为 next。
```
theme: next
```
到此，NexT 主题安装完成。下一步我们将验证主题是否正确启用。在切换主题之后、验证之前， 我们最好使用 hexo clean 来清除 Hexo 的缓存。

# [主题设定](https://theme-next.iissnan.com/getting-started.html#theme-settings)
## 主题样式
  编辑主题配置文件如下：
  ```
#---------------------------------------------------------------
#Scheme Settings
#---------------------------------------------------------------

#Schemes
#scheme: Muse
#scheme: Mist
#scheme: Pisces
scheme: Gemini

  ```
  选择Gemini主题
## 头像
  - 头像设置
     a 保存头像图片到`\MyBlog\themes\next\source\images`文件夹
	 b 编辑主题配置文件
	 ` avatar: /images/iroman.jpg `
  - 头像旋转
  进入路径打开文件：
```
  MyBlog\themes\next\source\css\_common\components\sidebarsidebar-author.styl
```
  编辑代码如下：
```
.site-author-image {
  display: block;
  margin: 0 auto;
  padding: $site-author-image-padding;
  max-width: $site-author-image-width;
  height: $site-author-image-height;
  border: $site-author-image-border-width solid $site-author-image-border-color;
  border-radius: 50%
  transition: 2s all;
}
.site-author-image:hover{
  transform: rotate(360deg);
}
.site-author-name {
  margin: $site-author-name-margin;
  text-align: $site-author-name-align;
  color: $site-author-name-color;
  font-weight: $site-author-name-weight;
}

.site-description {
  margin-top: $site-description-margin-top;
  text-align: $site-description-align;
  font-size: $site-description-font-size;
  color: $site-description-color;
}

```
  保存更新后，博客头像变成圆形，鼠标移到头像上方会使其旋转360度。
## 隐藏文章内容
	a 编辑主题配置文件
	  ```
#Automatically Excerpt. Not recommend.
#Please use <!-- more --> in the post to control excerpt accurately.
auto_excerpt:
  enable: true
  length: 100

	  ```
	b 在文章中使用下面语句截断文章，可保留格式。
	```
	<!-- more -->
	```
## 开启文章目录
  Hexo博客NexT主题中是有目录的，只是在默认情况下没有开启，需要我们来手动开启。
### 修改样式文件custom.styl
  文章目录样式文件custom.styl文件位于`themes/next/source/css/_custom`
  编辑代码如下：
  ```
.post-toc .nav .nav-child { 
  display: block; 
}
.post-toc ol {  
  font-size : 13px;     
} 
  ```
### 修改主题配置文件
  每行目录超长自动换行
  ```

# Table Of Contents in the Sidebar
toc:
  enable: true

  # Automatically add list number to toc.
  number: true

  # If true, all words will placed on next lines if header width longer then sidebar width.
  wrap: true

  ```
## 标题，作者以及链接
## 侧边栏社交链接
## 友情链接

# 文章编制
## 新建文章
`hexo n name`

# MarkDown语法
