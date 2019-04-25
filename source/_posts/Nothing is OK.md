title: 被Hexo折磨的一天
date: 2019/4/21
tags: 
- 吐槽
- HEXO
categories:
- HEXO
---
搞了一天终于把hexo同步了（划掉），实际上是从头再来ORZ

### 前情提要
自己的笔记本有安装Hexo，放在厦门。
公司的笔记本没安Hexo，却带回了家。
且GitHub上没有上传Hexo的源码。
心血来潮突然想更新博客，我该怎么搞？
答案：从头再来。
幸好博客上原本就只有一篇...

### 安装必备应用程序和必要步骤
安装Node.js，查看工具是否安装
$ node -v
安装Git
$ git --version
GitHub中配置名为<your_name>.github.io的repository[可百度]
GitHub中Setting->SSH and GPG keys配置SSH[可百度]


### 搭建Hexo
#### 使用npm指令安装hexo
$ npm install -g hexo-cli

#### 使用以下指令建站
$ hexo init <folder>    
$ cd <folder>
$ npm install

#### 建站后查看<folder>目录结构如下
```
.
├── _config.yml
├── package.json
├── scaffolds
├── source
|   ├── _drafts
|   └── _posts
└── themes
```
#### 配置参数
打开_config.yml,我配置下面这些参数
# 网站名称
title: 菜鸡的挣扎
# 作者名字
author: ThreeShu
# 时区，一定要写对
timezone: Asia/Shanghai
# 部署信息
deploy:
  type: git
  # 将要部署的仓库地址
  repo: https://github.com/yourname/yourname.github.io.git
  branch: master

### 本地搭建Git仓库
若你建站的文件夹名为Hexo，在Git中利用以下命令进入你的文件夹（当前在根目录下，我的Hexo在Y盘）
$ cd y:
$ cd Hexo
利用以下命令，初始化Git仓库
$ git init

#### 部署网站
写文章所用命令可查看官网https://hexo.io/zh-cn/docs/writing
每次对文件夹Hexo下的内容有做改动，利用以下命令就可以在localhost：4000本地查看页面修改后的状态
$ hexo c
$ hexo g
$ hexo s
利用以下命令部署到GitHub服务器后，访问yourname.github.io.git就可以看自己的博客了！
$ hexo d

#### 上传建站的源码至GitHub分支hexo
$ git add remote origin <远程仓库地址>
$ git add *
$ git commit -m "上传"
$ git push origin hexo

### 多机同步
$ mkdir <folder>
$ cd <folder>
$ git init
$ git clone <仓库地址>
$ npm install hexo-cli -g
$ npm install








