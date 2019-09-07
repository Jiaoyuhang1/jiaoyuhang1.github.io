---
layout:     post                    # 使用的布局（不需要改）
title:      Ubuntu更新pip失败               # 标题 
subtitle:    #副标题
date:       2019-09-07              # 时间
author:     YH                      # 作者
header-img: img/post-bg-2015.jpg    #这篇文章标题背景图片
catalog: true                       # 是否归档
tags:                               #标签
    - Ubuntu
    - pip
---

    ubuntu升级pip后， ImportError: cannot import name ‘main‘

原因是升级以后，路径变了，导致出错。

提示报错的是/usr/bin/pip，用which pip获取到的路径是～/.local/bin/pip

Traceback (most recent call last):
  File "/usr/bin/pip", line 9, in <module>
    from pip import main
ImportError: cannot import name main
~$ which pip
~/.local/bin/pip

解决办法很简单，把/usr/bin/pip替换为默认使用的pip即可，命令如下

sudo cp /usr/bin/pip /usr/bin/pip.bak && \
sudo cp ~/.local/bin/pip /usr/bin/pip

