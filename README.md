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
$ docker run -d -p 9000:9000 --privileged -v /var/run/docker.sock:/var/run/docker.sock 
