# 在centos上安装docker

## 一、卸载旧版本

```bash
sudo yum remove docker \
                docker-client \
                docker-client-latest \
                docker-common \
                docker-latest \
                docker-latest-logrotate \
                docker-logrotate \
                docker-engine
```

## 二、安装方法

有多种方式在安装docker

* 绝大多数用户设置docker仓库，然后从仓库安装，这是推荐的方式；
* 有些用户下载RPM包，然后手动安装，这种方式主要用来不联网安装；
* 为测试部署环境，有些用户选择脚本安装；


### 2.1 用仓库安装

```bash
sudo yum install -y yum-utils

sudo yum-config-manager \
    --add-repo \
    https://download.docker.com/linux/centos/docker-ce.repo
```

### 2.2 用包安装



## 最后、参考文件

1. 官方安装文档(https://docs.docker.com/engine/install/centos/)