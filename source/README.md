# CM BLOG

基于 Hexo 搭建，使用 [skapp](https://github.com/Mrminfive/hexo-theme-skapp) 主题。


# How to use


0. 首先你需要掌握：
   
   - Git 基础
   - npm 的使用
  
   
1. 项目分为两个分支，master 为博客主分支，hexo 为存放项目的分支

2. 首先 clone 整个项目到本地，并切到 hexo 分支

3. 参照 [Build up](#build-up) 部分完成构建

4. 现在你可以进行你对博客的操作，比如增删改查

5. 修改完毕之后，且 hexo s -l 本地检查无误后，即可 hexo g -d 进行更新 master 分支，即发布博客（**不能手动 push 到 master 分支**）

6. 然后可以使用 git 将本地的项目更新到 hexo 分支（hexo 分支即为保存项目的分支，不一定需要每次都更新，但是如果需要在另一设备管理博客，则在这之前就需要将最新的项目给 push 到 hexo 分支）

7. 当下一次使用的时候就可以直接跳到第四步开始了（注意，如果 hexo 分支在其他设备更新过，在操作前需要先 git pull 一下）


# Build up

**a**. 首先你需要掌握：

  - Hexo 基本用法
  - Hexo 主题相关
  - Markdown 语法基础
  - 基本的搜索能力
  - 附：[Hexo 官网](https://hexo.io/zh-cn/)、[此项目用到的 skapp 主题](https://github.com/Mrminfive/hexo-theme-skapp)                       


**b**. 现在你已经掌握上述技能，开始安装必要依赖：

  1. 由于使用 [nodejieba](https://github.com/yanyiwu/nodejieba) 分词库，所以 windows 下用户应提前安装好相应编译环境，即两个全局依赖：
  ```
  # 这里 Windows 下建议使用管理员身份打开命令行执行，可用 Win+X 打开
  # 安装太慢可用 cnpm ，后面同理
  npm install -g windows-build-tools
  npm install -g node-gyp
  ```

  1. 再装一堆项目依赖
  ```
  # 切到项目目录下（要保证处于 hexo 最新分支）执行：
  npm install --save hexo-autoprefixer hexo-filter-cleanup hexo-generator-feed hexo-generator-sitemap hexo-renderer-sass hexo-renderer-swig mamboer/lunr.js moment node-sass object-assign
  # 注意，安装 mamboer/lunr.js 可能会报错
  ```

  2. Warning：
  
    安装过程中可能会碰到一些问题，可自行解决

    附 issue：https://github.com/Mrminfive/hexo-theme-skapp/issues

    如果安装顺利，那你是真的流啤


**c**. 下载主题

  0. 因为之前已经配置好了，只需要把主题 clone 到 ./themes 里即可

  ```
  # 把主题 clone 到 ./themes 文件夹里
  cd themes && git clone https://github.com/Mrminfive/hexo-theme-skapp.git
  ```


**d**. 启动

  0. 确认你已经 npm install 过就可以跑起来了

  1. 如下：

```
# 清理缓存可用
hexo clean

# 跑在本地，如果这个项目有报错404，可加上 -l
hexo s

# 等同于 hexo generate
hexo g

# 等同于 hexo deploy
hexo d
```



# Base

- 每篇文章的基本配置如下：
```
title: Hello World 
cover: http://oxnuwmm3w.bkt.clouddn.com/hello-world.jpeg
# 作者信息，多作者则设置为数组
# 单作者
author: 
  nick: BruceYJ
  link: https://www.github.com/BruceYuj
# 多作者
author:
  - nick: BruceYJ
    link: https://www.github.com/BruceYuj
  - nick: minfive
    link: https://www.github.com/Mrminfive

# 如果文章为转载文章，需要多加文章出处项
editor:
  name: Minfive
  link: https://www.github.com/Mrminfive

# 首页每篇文章的子标题
subtitle: your subtitle
```


# Author

背锅人 @vzt7 - [vvzt666666@foxmail.com](mailto://vvzt666666@foxmail.com)


# Link

- 更多主题相关：https://github.com/Mrminfive/hexo-theme-skapp

