# docker-nmp
---
> 本内容适合在windows 环境下安装docker 并且构建完整的LNMP镜像，本镜像采用LNMP一键安装包 以及 Centos7.2 为系统 搭建

1. 运行构建命令

> docker build -t centos-lnmp /Users/liumeng/servers/docker_nmp/centos-lnmp/

2. 提交容器到镜像

> docker commit -a "liumeng" -m "centos-lnmp-1" 81514b7fbde5 centos-lnmp:v1

3. 启动新的镜像

>  docker run -d -i -t 75835a67d134 /sbin/init

4. 进入镜像可以使用

> docker attach
