---
title: first blog
date: 2017-01-19 21:39:46
categories: TEST
tags:
  -demo
  -common command
---

``` bash
hexo new "postName" #新建文章
hexo new page "pageName" #新建页面
hexo generate #生成静态页面至public目录
hexo server #开启预览访问端口（默认端口4000，'ctrl + c'关闭server）
hexo deploy #部署到GitHub
hexo help  # 查看帮助
hexo version  #查看Hexo的版本
```
<!-- more -->
修改推送到hexo分支

上一步的deploy参数正确配置后，文章写完使用 hexo g -d 命令就可以直接部署了，生成的博客静态文件会自动部署到 username.github.io 仓库的 master 分支上，这时候通过浏览器访问 http://username.github.io 就可以看到你的博客页面里。

网站页面是保存了，但这时候我们还没有保存我们的hexo原始文件，包括我们的文章md文件，我们千辛万苦修改的主题配置等。。。接下来使用下面的步骤将他们都统统推送到 hexo 分支上去

git add .

git commit -m “change description”

git push origin hexo

这样就OK了，我们的原始文件就都上去了，换电脑也不怕了。

日常写博客

有时候我们可能会在不同的电脑上写博客，那在不同的电脑上配置 hexo、git、node.js，以及配置git ssh key等都要折腾一下的，这是免不了的，也是比wordpress等其他博客框架麻烦的一点。

已有环境

如果在电脑上已经写过博客，那么可以在已有的工作目录下同步之前写的博客。在你的仓库目录下右键’git bash shell’，起来bash命令行，然后

git pull

这样你的状态就更新了，之后就是 hexo 命令写文章啦。。。

写完 hexo g -d 部署好后，使用

git add .

git commit -m “change description”

git push origin hexo

推送上去。

新的环境

到了新的电脑上时，我们需要将项目先下载到本地，然后再进行hexo初始化。

git clone https://github.com/dxjia/dxjia.github.io.git

cd dxjia.github.io

npm install hexo

npm install

npm install hexo-deployer-git –save

之后开始写博客，写好部署好之后，别忘记 git add , ….git push origin hexo…推上去。。。
