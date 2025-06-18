## Linux 基础学习
#### 系统关机、重启
> 重启：` reboot ` 或` shutdown -r now `
> 
> 关机：` shutdown -h now `或` power off `
> 
> `shutdown - r +30 ` 再过 30 分钟之后系统会重启，并显示后面的消息给所有在线用户
#### linux常用指令 
1. 查看当前linux发行版信息
```
 cat /etc/*-release
```

2. 查看linux内核信息
```
uname -r
```

3. 查看当前默认shell
列出系统当前所有可用的shell
```
chsh -l 或 cat /etc/shells
```

查看当前默认shell
```
echo $SHELL
```

4. 查看网卡信息及获取IP地址
```
dhclient 或 nmcli 或 ip a
```

5. 查看当前登录用户及切换登录用户
```
[vbird1@VM-16-17-centos ~]$ whoami
vbird1
[vbird1@VM-16-17-centos ~]$ su - root
Password:
Last login: Wed Jun 18 11:21:59 CST 2025 on pts/0
[root@VM-16-17-centos ~]# whoami
root
[root@VM-16-17-centos ~]# exit
logout
[vbird1@VM-16-17-centos ~]$
```
6. 查看主机名及更换主机名
```
[root@VM-16-17-centos ~]# hostname centos                    # 临时更换
[root@VM-16-17-centos ~]# hostname
centos
[root@VM-16-17-centos ~]# hostnamectl set-hostname centos    # 永久更换
[root@VM-16-17-centos ~]# cat /etc/hostname
centos
```

7. 查看当前工作目录
```
[root@VM-16-17-centos ~]# pwd
/root
[root@VM-16-17-centos ~]# su - vbird1
Last login: Wed Jun 18 14:24:32 CST 2025 from 221.12.4.143 on pts/0
[vbird1@centos ~]$ pwd
/home/vbird1
```

8. 切换目录
```
cd /          :切换工作目录
cd -          :返回切换前的目录
cd ~          ：回到家目录
cd ./         ：.代表当前目录
cd ..         ：放回上级目录
```

9. 更换密码
```
passwd                 :更换密码
passwd (whoami)        ：更换其他用户密码
passwd -d (whoami)     ：永久删除某个用户密码
```

