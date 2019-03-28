
<p align="center"><img src="./imgs/logo.png" alt="logo"></p>

<p align="center"><a href="https://nodejs.org/"><img src="https://img.shields.io/badge/node-10.13.0-brightgreen.svg" alt="node"></a> <a href="https://www.npmjs.com/"><img src="https://img.shields.io/badge/npm-6.4.1-brightgreen.svg" alt="npm"></a> <a href="https://hexo.io"><img src="https://img.shields.io/badge/hexo--cli-1.1.0-blue.svg" alt="hexo"></a></p>

<h2 align="center">cm blog</h2>

<p align="center">基于 <a href="https://hexo.io/">Hexo</a> 搭建，使用 <a href="https://github.com/miccall/hexo-theme-Mic_Theme">miccall</a> 主题</p>


## How to use

1. 首先你需要掌握：
   
   - Git 基础
   - npm 的使用
  
   
2. 项目分为两个分支，master 为博客主分支，hexo 为存放项目的分支

3. 首先 clone 整个项目到本地，并切到 hexo 分支

4. 参照 [Build up](#build-up) 部分完成构建

5. 现在你可以进行你对博客的操作，比如增删改查

6. 修改完毕之后，且 hexo s -l 本地检查无误后，即可 hexo g -d 进行更新 master 分支，即发布博客（**不能手动 push 到 master 分支**）

7. 然后可以使用 git 将本地的项目更新到 hexo 分支（hexo 分支即为保存项目的分支，不一定需要每次都更新，但是如果需要在另一设备管理博客，则在这之前就需要将最新的项目给 push 到 hexo 分支）

8. 当下一次使用的时候就可以直接跳到第四步开始了（注意，如果 hexo 分支在其他设备更新过，在操作前需要先 git pull 一下）


## Build up

**a**. 首先你需要掌握：

  - Hexo 基本用法
  - Hexo 主题相关
  - Markdown 语法基础
  - 基本的搜索能力
  - 附：[Hexo 官网](https://hexo.io/zh-cn/)、[此项目用到的 miccall 主题](https://github.com/miccall/hexo-theme-Mic_Theme)


**b**. 现在你已经掌握上述技能，开始搭建发布环境：

  0. 本地环境参考：

    - Node.js - v10.13.0 ( >= 8.x )
    - npm - v6.4.1 ( >= 6.x )
    - hexo-cli - v1.1.0

  1. 首先 clone 当前仓库，切换到 hexo 分支 ( ```git checkout hexo``` )，并执行 ```cnpm install```

  2. 此时获取主题 ( 已经将 theme repo 添加为 submodule 不需要自己手动复制了:) )
  ```
  # 通过子模块更新主题
  git submodule update
  ```

  3. 将 ```_config_theme.yml``` 中的内容 `复制并覆盖` 到 ```./themes/hexo-theme-Mic_Theme/_config.yml```  ( 修改主题里的 config 文件后也要记得同步根目录下的 config )

  4. OK

**c**. 启动！

```
# 清理缓存可用
hexo clean

# 在本地启动
hexo s

# hexo g 等同于 hexo generate
hexo g

# hexo d 等同于 hexo deploy
hexo d

# hexo g -d 等同于 hexo g + hexo d
hexo g -d
```



## Base

- 每篇文章的基本配置如下：
```
---
title: # 文章标题  
date: 2019-3-28 19:22:28  # 文章发表时间
tags:
- 标签1
- 标签2 (可选)
categories: Algorithm # 分类
thumbnail: https://xxxxxxxxxx.png # 略缩图
---

文章正文
```


## Author

背锅人 @vzt7 - [vvzt666666@foxmail.com](mailto://vvzt666666@foxmail.com)