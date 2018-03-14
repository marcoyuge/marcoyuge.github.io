---
layout:     post
title:      "欢迎来到我的博客"
subtitle:   " \"Hello World, Hello Blog\""
date:       2018-03-13 
author:     "Yu"
header-img: "img/post-bg-2015.jpg"
tags:
    - 生活
---

> “Hello blog！ ”


## 前言

忙活了一天，总算把博客搞定上线了。（虽然大部分都是瞎忙活）  

---

## 正文

这个博客的灵感来自于知乎上的[这个回答](https://www.zhihu.com/question/26033776/answer/35484765)。思路是用[GitHub Pages](https://pages.github.com/) + [Jekyll](http://jekyllrb.com/) 快速上线个人Blog 的技术方案。

其优点非常明显：

* **Markdown** 带来的优雅写作体验
* 非常熟悉的 Git workflow ，**Git Commit 即 Blog Post**
* 利用 GitHub Pages 的域名和免费无限空间，不用自己折腾主机
* 如果需要自定义域名，也只需要简单改改 DNS 加个 CNAME 就好了
* Jekyll 的自定制非常容易，基本就是个模版引擎


---

配置的过程中基本参照网上的教程，也遇上过一些[坑教程](http://blog.csdn.net/walkerhau/article/details/77394659?utm_source=debugrun&utm_medium=referral)，写的过程不详细，一旦过程中配置错误，基本要回滚之前好几次的操作。不过这个过程也了解了不少GitHub的错误命令(mmp)  
<div align="center"><img src="https://i.loli.net/2018/03/13/5aa7ee6479466.png" width="80%"></div>


 + 安装 ruby 和 jekyll的过程十分简单，基本上是和配置 git 的 repo 同时进行，然而两边进行的都不太顺利。先是ruby装错了版本，装上了旧版本的 dev-kits 之后再**`gem install jekyll `**，才发现 Jekyll 并不支持旧版本 ruby。(????)  
 <div  align="center">    
<img src="https://i.loli.net/2018/03/14/5aa939f12422d.jpg" width="30%"/>
</div>


+ 重新装上更新稳定版 ruby，和相关的 MSYS2+MinGW64 开发环境，才顺利装上了 Jekyll。Jekyll 主题上直接 fork 了 hux Blog 的主题，如果不需要在本地调试博客可以不用装 Jekyll。  

* 装好Jekyll之后在本地博客根目录下执行命令**`jekyll serve --watch`**就可以直接在**127.0.0.1:4000** 地址上看见自己博客的上线效果（并且支持修改后实时变化，相比把修改push到repo然后等github pages的更新更快）


最后就在本地调试好博客，让博客正常显示就哦了。写博客需要用到[markdown](http://www.markdown.cn/)，一个相当简洁直观的从文本转到html文档的工具。  

编辑markdown文档可以使用[**sublime text 3**和插件对编辑内容进行实时预览](http://blog.csdn.net/github_32886825/article/details/52930195) 



## 后记

回顾这个博客的诞生，纯粹是出于个人兴趣。在知乎相关问题上回答并获得一定的 star 后，我决定把这个博客主题当作一个小小的开源项目来维护。

在经历 v1.0 - v1.5 的蜕变后，这个博客主题愈发完整，不但增加了诸多 UI 层的优化（opinionated）；在代码层面，更加丰富的配置项也使得这个主题拥有了更好的灵活性与可拓展性。而作为一个开源项目，我也积极的为其完善文档与解决 issue。

如果你恰好逛到了这里，希望你也能喜欢这个博客主题。

—— Yu 后记于 2015.10
