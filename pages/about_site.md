---
layout: page
title: "关于本站点的建设方式"
description: "一个基于github.io搭建的个人静态网站"
---


# 关于站点

  本站点是`四无浪子`个人网站，通过github提供的静态站点托管服务。内容由markdown 编写，通过Jekyll转化为html页面。
所有代码都存放在github空间：<https://github.com/deonwu/deonwu.github.io>.


# 在github上托管静态页面

  只需要在github上创建一个“github.io” 结尾的项目名（例如:deonwu.github.io)。就可以将静态html作为提交到代码仓库。然后通过github.io这个域名进行访问了。具体的操作方参考文档：<https://pages.github.com/> .

  还可以申请一个自己的域名，通过CNAME 绑定到github.io 这个域名。例如本站的域名是(deonwu84.com) 访问在github上的网页。当然在域名生效前，还需要在github上做一个简单的设置。参考文档: <https://help.github.com/articles/quick-start-setting-up-a-custom-domain/>


# 通过Jekyll将Markdown转化为HTML

Markdown是一种普通文本编辑的标记语法，很多技术文档都通过这种语法编写。Jekyll是一个Ruby写的静态页面博客程序，没有数据库功能，只是将Markdown文本转换为html页面。

Jekyll的安装参考文档<https://jekyllrb.com/docs/>。

1. 通过gem 安装jekyll 和bundle。
  ```
  gem install jekyll bundler
  ```
2. 本地运行服务
  ```
  bundle exec jekyll serve
  ```
3. 在`~/.profile`中设置一个快捷命令启动jekyll
  ```
  alias run_site='cd ~/works/gitlab/deonwu.github.io && bundle exec jekyll serve'
  ```