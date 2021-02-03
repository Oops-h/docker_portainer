# docker_portainer
Learning docker and deploy portainer on Tencent Cloud
学习docker并在腾讯云搭建portainer docker可视化web
# 安装docker 
这里使用官方脚本一键安装
$ curl -sSL https://get.docker.com/ | sh
等待脚本执行完毕后，测试hello world 镜像
$ docker run hello-world
# 测试成功



安装portainer
拉取portainner 镜像
$ docker pull portainer   
下载完成后运行portainer
$ docker run -d -p 9000:9000 --privileged -v /var/run/docker.sock:/var/run/docker.sock 
