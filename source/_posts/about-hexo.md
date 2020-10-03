---
title: about_hexo
date: 2020-09-25 21:43:14
tags:
---

### 安装 hexo
使用npm命令安装Hexo，输入：
`npm install -g hexo-cli`
安装完成后，初始化我们的博客，输入：
`hexo init blog`
(这里的命令都是作用在刚刚创建的Blog文件夹中。)

### Hexo 命令
`npm install hexo -g`  #安装Hexo
`npm update hexo -g`    #升级
### 命令简写
hexo n "我的博客" == hexo new "我的博客" #新建文章
hexo g == hexo generate #生成
hexo s == hexo server #启动服务预览
hexo d == hexo deploy #部署
hexo server #Hexo会监视文件变动并自动更新，无须重启服务器
hexo server -s #静态模式
hexo server -p 5000 #更改端口
hexo server -i 192.168.1.1 #自定义 IP
hexo clean #清除缓存，若是网页正常情况下可以忽略这条命令

### 与github关联

![](https://ftp.bmp.ovh/imgs/2020/09/16948e4b0b7e9d8a.png)

deploy:
type: git
repo: 这里填入你之前在GitHub上创建仓库的完整路径，记得加上 .git
branch: master参考如下：

![](https://ftp.bmp.ovh/imgs/2020/09/bfc99ffe28f3633f.png)

#### 保存站点配置文件
其实就是给hexo d 这个命令做相应的配置，让hexo知道你要把blog部署在哪个位置，很显然，我们部署在我们GitHub的仓库里。最后安装Git部署插件，输入命令：
`npm install hexo-deployer-git --save`

这时，我们分别输入三条命令：
```
hexo clean 
hexo g 
hexo d
```
其实第三条的 hexo d 就是部署网站命令，d是deploy的缩写。完成后，打开浏览器，在地址栏输入你的放置个人网站的仓库路径，即 http://xxxx.github.io 
你就会发现你的博客已经上线了，可以在网络上被访问了。




