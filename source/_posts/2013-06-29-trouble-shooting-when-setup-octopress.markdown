---
layout: post
title: "设置octopress环境遇到的问题"
date: 2013-06-29 12:49
comments: true
categories: 
---

###Failed to connect to toolbelt.heroku.com

当执行以下命令安装Ruby时，我一直出现连接toolbelt.heroku.com失败，尝试了N种方案，换网络，加代理，走VPN，走Goagent均失败:

```
curl -L https://get.rvm.io | bash -s stable --ruby
```

or

```
rvm install 1.9.3
```

最后使用一牛人的脚本搞定:

<http://www.isotope11.com/blog/update-v1-dot-0-1-quickly-get-a-fresh-ubuntu-install-ready-for-ruby-dev>


###Liquid Exception: incompatible character encodings: UTF-8 and ISO-8859-1 in post

当调用_rake generate_时可能会出现这个错误，因为jekyll默认不支持中文，在_.bash_profile_中添加以下环境变量即可解决：

```
export LC_ALL=en_US.UTF-8
export LANG=en_US.UTF-8
```

