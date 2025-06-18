## Linux 基础指令学习
#### 系统关机、重启
> 重启：` reboot ` 或` shutdown -r now `
> 
> 关机：` shutdown -h now `或` power off `
> 
> `shutdown - r +30 ` 再过 30 分钟之后系统会重启，并显示后面的消息给所有在线用户
#### linux基本信息查询 
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

4. 

