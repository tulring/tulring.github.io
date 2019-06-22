---
title: GitHub使用
subtitle: GitHub注册
description: 网站描述
date: 2019-06-17 14:53:29
tags:
	- 导航
	- GitHub
categories: GitHub
---
# GitHub搭建环境
## GitHub注册
## Git软件安装
* 下载Git软件
  [下载链接](https://git-scm.com/downloads)
 
* 安装
   全程默认设置
  
# Git使用
## 获取SSH公钥
`$ ssh-keygen -t rsa -C "your_email@youremail.com"`
## 添加SSH公钥到github
验证公钥添加是否成功：
`$ ssh -T git@github.com`
## 设置username和useremail
``` 
$ git config --global user.name "your name"
$ git config --global user.email "your_email@youremail.com"
```
## 上传本地文件到github仓库
### 进入github主页新建仓库
新建仓库后记录仓库地址：
   `https://github.com/wangle1218/×××××××××.git`
### 进入要上传的文件夹，初始化上传文件夹仓库
   `$ cd ../python/machineLearningCode/`  
   `$ git init`
### 编辑要上传的文件代码
### 添加要上传的文件到git
   将文件添加到暂存区(Index)
	 `$ git add .`
	 将暂存区文件提交到HEAD
	 `$ git commit -m "XXXX"`
### 连接到github仓库
   `$ git remote add origin https://github.com/wangle1218/********.git`
### 上传文件
`$ git push -u origin +master`
## 修改代码
### 修改代码源文件
### 重新上传到github仓库
注意标明跟新说明

## 查看历史版本
### 进入仓库主页
### 点击History
### 选择历史版本，点击<>
### 点击Clone or download即可下载历史版本代码
## 分支(Branch)
### 创建分支并且换过去
`$ git checkout -b branch`
### 切回主分支
`$ git checkout master`
### 删除分支
`$ git branch -d branch`
### 推送分支到github
`$ git push origin branch`
### 合并分支内容到当前分支
`$ git merge branch`