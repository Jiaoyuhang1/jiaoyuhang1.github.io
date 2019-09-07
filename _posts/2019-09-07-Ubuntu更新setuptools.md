---
layout:     post                    # 使用的布局（不需要改）
title:      Ubuntu更新setuptools               # 标题 
subtitle:    #副标题
date:       2019-09-07              # 时间
author:     YH                      # 作者
header-img: img/post-bg-2015.jpg    #这篇文章标题背景图片
catalog: true                       # 是否归档
tags:                               #标签
    - Ubuntu
    - setuptools
---
    
输入sudo pip3 install setuptools==34，却一直提示Found existing installation: setuptools 20.7.0，无法升级到30以上的版本。应该用sudo easy_install --upgrade setuptools来升级。
