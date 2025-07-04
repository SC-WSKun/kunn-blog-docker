# Kunn Blog Docker

参考的`https://chunchengwei.github.io/ruan-jian/ji-yu-docker-de-hexo-bo-ke-da-jian/`搭建的博客项目

## 环境准备

1. 安装 Docker
2. 准备博客文件夹，路径位于`$HOME/MyBlog`，可以自己在`docker-compose.yml`中更改

## 博客格式
1. 博客文件夹中按照分类(Catogery)分别建立文件夹放置各分类的Markdown文档
2. 文档格式如下（可以用 hexo new 命令自动生成带模板的文档）:
```markdown
---
title: ''
date: YYYY-MM-DD HH:MM:SS
tags: ''
categories: ''
---
```

## 运行命令

1. 初始化 Hexo 环境，构建基础镜像
```shell
docker build -t 'hexo-base:18' -f Dockerfile_base .
```
2. 打包博客进新的镜像
```shell
docker build -t 'kunn-hexo-blog:v1' -f Dockerfile_blog .
```
3. 运行容器
```shell
docker compose up -d
```

## 个性化修改

个人信息可以在`theme/hexo-theme-kaze/_config.yml`中修改
