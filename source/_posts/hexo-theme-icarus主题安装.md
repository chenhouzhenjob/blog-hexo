---
title: hexo-theme-icarus主题安装
date: 2024-05-15 18:15:22
tags: 
- hexo
- icarus
categories:
- hexo
#封面图
cover: /file/icarus_page.png
# 缩列图
# thumbnail: /file/icarus_page.png
---

`hexo-theme-icarus` 是一个简约的主题
<!-- 之上是简介 -->
<!-- more -->


{% img /file/icarus_page.png "icarus样式图" %}
icarus 主题安装后，

# 安装
## 通过源码安装
根据官网的介绍，通过源码安装的话只需要再hexo主执行下执行
```
git clone https://github.com/ppoffice/hexo-theme-icarus.git themes/icarus -b <version number> --depth 1
```
如果你只是想下载最新版本的话，可以去掉 `-b <version number>`，`--deptch 1` 是和 Git相关，如果不介意下载全部Git的提交记录的话，这个也可以不要，简化后使用
```
git clone https://github.com/ppoffice/hexo-theme-icarus.git themes/icarus
```

这条命令会把 hexo-theme-icarus 项目下载到 themes 目录下

然后我们可以有两种方式切换到 icarus 主题上
第一种方式： 修改 _config.yml 文件激活 Icarus主题
```_config.yml
theme: icarus
```

第二种方式：通过执行 hexo 命令切换主题
```
hexo config theme icarus
```
其实这个命令的本质也是修改 ——config.yml文件

这样子就完成了，可以执行下面的命令来 启动 Hexo 本地服务器
```
hexo server
```

但是，这种方式你后面无法直接去修改 icarus 里的源码

可以采用 git submodule ，

git submodule 是一个很好的多项目使用共同类库的工具，它允许类库项目做为repository,子项目做为一个单独的git项目存在父项目中，子项目可以有自己的独立的 commit ， push ， pull


### 源码介绍

## 通过NPM安装
如果我们不需要修改源码的话，推荐采用 NPM的安装方式，这个操作下来更简单。



```
npx patch-package hexo-theme-icarus
```

会 生成 patches 目录 记录修改文件的 diff
[通过NPM安装](#源码介绍)