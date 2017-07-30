---
layout: default
title: Mac下使用jekyll在github上建博客
category: article
---

<p><font size="6">为了</font>更好地展示自己的项目，GitHub带有GitPage功能用来方便用户使用静态页面进行项目的展示。</p>

就是因为这个功能的存在，我们才能够在这个上面建立我们自己博客，无论是个人文档、项目的展示还是在求职中让自己的简历有锦上添花的效果，都是值得我们去尝试的。顺道说一句，或许由于各种原因，我们并不能够很便捷地访问GitHub，国内不少开源网站也纷纷建立起自己的git管理系统来方便国内开源开发者进行代码的共享和学习，比如gitcafe、coding、oschina，但是笔者并没有发现这些网站上有免费的GitPage的功能，也就没有去进一步百度。<br>

那么，我们就开始欢乐地建立我们自己的博客吧～～<br>

在开始前，我需要准备建站的你具有这些知识：如何使用<a href="https://git-scm.com/">git</a>，以及<a href="https://github.com/">github</a>究竟是不是最大的同性交友网站。对于不能够顺利翻墙的Mac用户来说，需要有使用gem和homebrew的经验(不会的话复制命令总会吧),如果你碰巧满足这些条件，OK,here we go!<br>

* 我们需要有一个GitHub的账号，没有的话请点击<a href="https://github.com/join?source=header-home">Sign up</a>进行注册，成功登陆GitHub后，创建一个新的仓库<br/>![创建新仓库](../../../../images/img-07-28.png)
* 仓库名称为[你的用户名].github.io，协议选择GNU General Public Lisence v2.0，记得勾选上初始化README选项，点击Create reposltory创建仓库。创建成功后你输入网址[你的用户名].github.io会有和你的网址一样显示的网页<br/>![创建新仓库](../../../../images/img-07-28-01.png)
* 接下来，打开你的命令行窗口，或许有不少人没用过gem进行软件的安装，这样建议更改gem源进行gem的更新，命令为：<br/><code>gem sources --remove https://rubygems.org/</code><br/><code>gem sources --add https://gems.ruby-china.org/</code><br/><code>gem update --system</code><br/>其中第三条命令如果运行不成功在前面sudo，运行后需要耐心等待一段时间。然后安装jekyll，命令为<code>gem install jekyll</code>
* 安装成功后，在<a href="http://jekyllthemes.org/">这个网站</a>寻找你想要使用的模版并下载到本地
* 在命令行下进入解压后的文件夹，git初始化文件夹。此时，假如没有特别的需求，就可以只是在_post文件夹里写我们的文章，记得文章名字要符合yy-mm-dd-xxxx.md，这些模版会在主页自动检索_post文件夹下所有的文件并显示在主页上。当然假如你有更多的需求，可以自己研究这些页面进行适当的修改
* 简单介绍一下.md文件，这个是markdown文件，具体<a href="http://www.appinn.com/markdown/">markdown语法</a>请自行了解，而如何用jekyll更好更方便写出漂亮的文章，请参考<a href="http://yansu.org/2014/02/12/how-to-deploy-a-blog-on-github-by-jekyll.html">这个网站</a>，这里就不在赘述了。