---
layout: post
title: "初识树莓派"
date: 2018-05-19
description: "Raspberry Pi 初尝试"
tag: 树莓派 
---   

　　第一次听说树莓派是在我大一的时候，那时对他的了解也仅限于听说过，知道树莓派是创客经常使用的单片机而不是面包房里的水果派，然后就跳入了51的坑。在大二上学期的时候实验室进了一批树莓派套件，用于做AGV小车协同控制开发，这才第一次见到树莓派的真身。
   
　　简单来说树莓派就是一台微型电脑，详细情况网上都有我就不复制粘贴了，这里有两个很全面介绍链接可以去了解一下：[树莓派-Wiki](https://www.wikiwand.com/zh/%E6%A0%91%E8%8E%93%E6%B4%BE)、[树莓派-百度百科](https://baike.baidu.com/item/Raspberry%20Pi)。我手上拿到的是3B，当时的最新款是性能最好的（可见学校还是很土豪的），当然现在的话又发布了性能更好的3B+，考虑找老师再去买几块嘿嘿嘿。
   
　　目前AGV是另一个小组在做，但是板子很多，所以我也拿了一块，闲暇时调戏一下。目前仅是拿来个人娱乐，所以目的性会比较强，等后面再系统地学习吧。
   
## 一 搭建可道云储存平台

背景：经常有上机实验需要拷贝一些文件，U盘携带不便，就想拿树莓派作为服务器搭建一个个人云，利用学校的局域网进行文件管理，局域网内网速也特别快。

参考资料：[可道云](https://kodcloud.com/)      [lnmp环境搭建](https://lnmp.org/install.html)
            
### 一，使用lnmp一键安装包安装所需环境
`官网：https://lnmp.org/`
~~~
wget -c http://soft.vpser.net/lnmp/lnmp1.4.tar.gz && tar zxf lnmp1.4.tar.gz && cd lnmp1.4 && ./install.sh lnmp
//可道云并不需要数据库，可以选择不安装，PHP版本建议选7.0以上
//此过程较慢，大概需要3小时
~~~
完成后，在浏览器输入树莓派ip会出现lnmp默认页

### 二，下载并安装可道云

下载可道云(版本号可自定义)

`wget http://static.kalcaddle.com/update/download/kodexplorer4.25.zip`

解压可道云到指定目录/home/wwwroot/default/

`unzip kodexplorer3.46.zip -d /home/wwwroot/default/`

此时，在浏览器输入`树莓派ip//index.php`可以进入可道云登陆页面

### 三，删除index.html文件

　　在实际执行中，好像无法删除，则重命名即可。

### 四，完成
　　在执行过程中以root权限进行，必要时设置777权限。

   
    
 
　　
