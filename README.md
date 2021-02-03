# docker_portainer
学习docker并在腾讯云搭建portainer docker可视化web管理后台

# 安装docker 
这里使用官方脚本一键安装

$ curl -sSL https://get.docker.com/ | sh

等待脚本执行完毕后，测试hello world 镜像

$ docker run hello-world

测试成功




# 安装portainer
查找portainner 镜像

$ docker search portainer

$ docker pull portainer/portainer-ce(以为第一个版本会收费，所以选择ce版本)

下载完成后运行portainer

$ docker run -d -p 9000:9000 --privileged -v /var/run/docker.sock:/var/run/docker.sock portainer/portainer-ce

-d: 后台运行容器，并返回容器ID

-p: 指定端口映射，格式为：主机(宿主)端口:容器端口;

--privileged 让container内的root拥有真正的root权限

-v 本地目录:容器目录  或 -v 容器目录

/var/run/docker.sock它是Docker守护进程(Docker daemon)默认监听的Unix域套接字(Unix domain socket)，容器中的进程可以通过它与Docker守护进程进行通信。

Portainer通过绑定的/var/run/docker.sock文件与Docker守护进程通信，执行各种管理操作
关于/var/run/docker.sock 可参考文章
https://www.cnblogs.com/fundebug/p/6723464.html

# 成功运行部署portainer
进入腾讯云9000端口查看是否成功
http://42.193.184.8:9000
