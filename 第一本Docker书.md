###### 简介

###### 安装Docker

> 前提条件，CPU必须是64位，centos3.10以上。
```bash
[**@** /]$ uname -a  #查看内核版本
[**@** /]$ sudo yum update  #升级系统
[**@** /]$ sudo reboot  #重启服务后再次查看内核版本
[**@** /]$ sudo systemctl docker start #启动docker守护线程
[**@** /]$ sudo systemctl enable docker #设置开机启动
[**@** /]$ docker info  #确认docker是否正确安装并运行
```
###### Docker入门
```bash
[**@** /]$ docker pull ubuntu  #下载一个ubuntu镜像
[**@** /]$ docker ps -a  #查看docker容器信息，添加-a查看所有，否则只查看启动的容器
[**@** /]$ man docker-run  #查看运行docker容器命令
[**@** /]$ sudo docker run #name brave -i -t ubuntu /bin/bash  #创建一个新的ubuntu container容器，i输入t分配一个伪tty终端,给容器命名
root@**:/#  hostname  #查看容器主机名
root@**:/# ip a  #查看ip地址
root@**:/# ps -aux  #查看容器进程
root@**:/# exit  #退出Docker容器
[**@** /]$ sudo docker start brave  #重新start已经停止的容器
[**@** /]$ docker attach #sig-proxy=false brave  #连接到正在运行的容器中
[**@** /]$ docker run #name brave -d ubuntu /bin/bash -c "while true; do echo hello world; done"  #创建守护容器-d
[**@** /]$ docker logs #tail -ft brave  #查看日志
[**@** /]$ docker rm brave  #移除容器
[**@** /]$ docker rm $(docker ps -a -q)  #删除所有停止的容器
[**@** /]$ sudo docker top daemon_dave  #查看守护式容器的进程
```
###### 使用Docker镜像和仓库
```bash
[**@** /]$ docker images  #列出所有镜像
```
###### 在测试中使用Docker

###### 使用Docker构建服务

###### 使用Fig编配Docker

###### 使用Docker API

###### 获取帮助和对Docker进行改进
