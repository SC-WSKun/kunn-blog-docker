# Kunn Blog Docker

参考的`https://chunchengwei.github.io/ruan-jian/ji-yu-docker-de-hexo-bo-ke-da-jian/`搭建的博客项目

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