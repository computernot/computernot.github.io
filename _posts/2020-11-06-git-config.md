---
layout:     post
title:      "Git config"
subtitle:   "给git（包含cocoapods）加上代理"
date:       2020-11-06 15:34:18
author:     "CC"
header-img: "img/home-bg-geek.jpg"
catalog: false
tags:
    - git
    - cocoapods
---

# Cocoapods 速度慢解决方法
cocoapods速度慢，主要问题还是墙的问题，加代理后可基本解决问题

查看当前的git配置
```sh
git config --global --list
```

假如代理地址为 `http://127.0.0.1:7890`
<br/>
给git加上代理(包含http和https)
```sh
git config --global http.https://github.com.proxy http://127.0.0.1:7890
```

移除git代理
```sh
git config --unset --global http.https://github.com.proxy
```
