# Linux

## firewall
```
启动
systemctl start firewalld
重启
systemctl restart firewalld
查看状态
systemctl status firewalld
停止
systemctl disable firewalld
禁用
systemctl stop firewalld
查看80端口是否开启
firewall-cmd --query-port=80/tcp --zone=public
开启某端口代码
firewall-cmd --zone=public --add-port=80/tcp --permanent 
```

## lsof
```
查看8080端口占用
lsof -i:8080
显示开启文件abc.txt的进程
lsof abc.txt
显示abc进程现在打开的文件
lsof -c abc
列出进程号为1234的进程所打开的文件
lsof -c -p 1234
显示归属gid的进程情况
lsof -g gid
显示目录下被进程开启的文件
lsof +d /usr/local/
同上，但是会搜索目录下的目录，时间较长
lsof +D /usr/local/
显示使用fd为4的进程
lsof -d 4
显示所有打开的端口和UNIX domain文件
lsof -i -U
```

## netstat
```
查看当前所有tcp端口
netstat -ntlp
查看所有80端口使用情况 u -udp
netstat -ntulp | grep 80
```

## kill
```
kill -9 PID
killall -9 进程名
```

## mv
```
命令格式：mv [-fiv] source destination
    参数说明：
    -f:force，强制直接移动而不询问
    -i:若目标文件(destination)已经存在，就会询问是否覆盖
    -u:若目标文件已经存在，且源文件比较新，才会更新
```

## cp
```
文件复制命令cp
    命令格式：cp [-adfilprsu] 源文件(source) 目标文件(destination)
              cp [option] source1 source2 source3 ...  directory
    参数说明：
    -a:是指archive的意思，也说是指复制所有的目录
    -d:若源文件为连接文件(link file)，则复制连接文件属性而非文件本身
    -f:强制(force)，若有重复或其它疑问时，不会询问用户，而强制复制
    -i:若目标文件(destination)已存在，在覆盖时会先询问是否真的操作
    -l:建立硬连接(hard link)的连接文件，而非复制文件本身
    -p:与文件的属性一起复制，而非使用默认属性
    -r:递归复制，用于目录的复制操作
    -s:复制成符号连接文件(symbolic link)，即“快捷方式”文件
    -u:若目标文件比源文件旧，更新目标文件
```

## install

### nvm
```
wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash
添加环境变量
source ~/.bashrc
```
### nginx
```
wget http://nginx.org/download/nginx-1.19.10.tar.gz
解压
tar -zxvf nginx-1.8.0.tar.gz
```
### git
```
yum install git
```
### nginx
```
yum install nginx
```
### frp
```
wget https://github.com/fatedier/frp/releases/download/v0.36.2/frp_0.36.2_linux_amd64.tar.gz
解压
tar -zxvf frp_0.36.2_linux_amd64.tar.gz
```