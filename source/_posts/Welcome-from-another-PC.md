---
title: Welcome from another PC
date: 2017-02-08 18:41:14
categories: TEST
tags:
---
1、关于日常的改动流程
2、本地资料丢失后的流程<!-- more -->
在本地对博客进行修改（添加新博文、修改样式等等）后，通过下面的流程进行管理。
添加新博文`hexo new "postName"`,然后修改对应的md文件。文件目录：/source/_posts
1. 依次执行
```
git add .
git commit -m "..."
git push origin hexo
```
指令将改动推送到GitHub（此时当前分支应为hexo）；//本文为hexxoo。
2. 然后才执行`hexo g -d`发布网站到master分支上。


虽然两个过程顺序调转一般不会有问题，不过逻辑上这样的顺序是绝对没问题的（例如突然死机要重装了，悲催....的情况，调转顺序就有问题了）。

三、本地资料丢失后的流程
当重装电脑之后，或者想在其他电脑上修改博客，可以使用下列步骤：

1. 使用`git clone git@github.com:echoorchid/echoorchid.github.io.git`拷贝仓库（默认分支为hexo）；
2. 在本地新拷贝的http://echoorchid.github.io文件夹下通过Git bash依次执行下列指令：
```
npm install hexo
npm install
npm install hexo-deployer-git # (记得，不需要hexo init这条指令）。
```
