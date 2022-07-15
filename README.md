# DjangoProject

使用Django搭建的网页小游戏~

[toc]

## 简介

基于Django框架实现类似坦克大战小游戏，试玩地址：https://app2215.acapp.acwing.com.cn/

### 功能介绍

#### 登录与注册

正常登录注册以及接入第三方API实现一键登录。

#### 游戏模式

分为单人模式和多人模式。

**单人模式**：5个简单AI随机移动或攻击，不能使用闪现技能，不支持聊天窗口。

**多人模式**：最少需要3名玩家，可以多开，等待匹配成功后开始游戏。支持聊天窗口。









----------------------

#### 租服务器
阿里云、华为云或腾讯云

#### 安装Docker
官方教程 [Ubuntu安装](https://docs.docker.com/engine/install/ubuntu/)
##### Docker常用命令：
docker容器运行后无法添加端口。可先将容器生成镜像，然后再重新生成容器。 
###### 镜像（images）  

- `docker images`：**列出本地所有镜像**   
- `docker pull ubuntu:20.04`：**拉取一个镜像**（ubuntu是镜像名称，：后面是版本号）  
- `docker image rm ubuntu:20.04`：**删除一个镜像**
- `docker [container] commit CONTAINER IMAGE_NAME:TAG`：**创建某个container的镜像**
- `docker load -i ubuntu_20_04.tar`：**将镜像ubuntu:20.04从本地文件ubuntu_20_04.tar中加载出来**
- `docker save -o ubuntu_20_04.tar ubuntu:20.04`：**将镜像ubuntu:20.04导出到本地文件ubuntu_20_04.tar中**

###### 容器（container）

- `docker [container] create -it ubuntu:20.04`：**利用镜像ubuntu:20.04创建一个容器。**
- `docker ps -a`：**查看本地的所有容器**
- `docker [container] start CONTAINER`：**启动容器**
- `docker [container] stop CONTAINER`：**停止容器**
- `docker [container] attach CONTAINER`：**进入容器** (先按Ctrl-p，再按Ctrl-q可以挂起容器)
- `docker [container] rm CONTAINER`：**删除容器**

最后在docker中创建账户并添加sudo权限。

#### 服务器配置配置免密登录
生成公钥和密钥：`ssh-keygen`.并在`.ssh/`目录下创建config

添加如下内容：
```
Host : 免密登录别名
    Hostname ： IP地址
    User ： 登录账户
    Port ： 开放的端口号
```

