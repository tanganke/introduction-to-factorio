# Linux

在这里，我将介绍如何搭建Linux系统下的专用服务器。
如果和好友都在同一局域网下游玩（这种情况一般是通过同一路由器上网），也可以使用Linux虚拟机（网卡设置为桥接）。
否则，您应该准备一台具有公网IP的Linux服务器（可以在腾讯云、阿里云等云服务器商获取）或使用Linux虚拟机/WSL+内网穿透的方案。
建议至少是双核处理器，有2G及以上的内存，以及5Mbps及以上的带宽。

## 方法一：使用docker容器

### 安装docker

如果你是Ubuntu用户，可以使用以下命令安装docker：

```bash
sudo apt install docker.io
```

这将安装Docker并启动Docker服务。您可以使用以下命令检查Docker是否已成功安装：

```bash
docker --version
```

如果你是其他Linux发行版的用户，请参考[官方文档](https://docs.docker.com/engine/install/)。
如果您需要更多关于Docker的信息，您可以查看Docker官方文档。在文档中，您可以找到有关如何使用Docker的详细信息，以及如何构建和运行Docker容器。如果您遇到任何问题，您可以在Docker论坛上寻求帮助，或者在Docker社区中与其他用户交流。


### 下载镜像

```bash
docker pull factoriotools/factorio
```

### 运行容器

```bash
docker run -d \
    -p 34197:34197/udp \
    -p 27015:27015/tcp \
    -v /opt/factorio:/factorio \
    --name factorio \
    --restart=always \
    factoriotools/factorio
```

### 客户端连接服务器

在游戏主菜单中，点击“多人游戏”，然后点击“服务器直连”，在“IP地址”中输入服务器的IP地址，点击“加入游戏”即可。


## 方法二：下载专用服务器程序

[从官方下载专用服务器（Headless server）](https://www.factorio.com/download/archive/)，请注意选择和游戏客户端对应的版本。
