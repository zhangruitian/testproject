# Build Project
**********  

## Build Server Environment 
**********  

### Server selection
* **Intranet**  

Raspberry Pi OS(Raspbian) - based on Debian  

* **Public network**  

CentOS  

### Node  

1. install **nvm** which manage node version  

```shell
wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash
source ~/.bashrc  // config as global value
```

2. install **Node**  

```shell
nvm list-remote // list all version in nvm library
install x.x.x  // download node, such as 15.14.0
```

### Git  

1. install  

```shell  
apt-get install git  // on Debiam
yum install git  // on CentOS
```

### Nginx  
1. install  

```shell
apt install nginx  // on Debiam
yum install nginx  // on CentOS
```

2. nginx config file  

* destinaion: /etc/nginx/nginx.conf  
> How to config ?  
> Coming soon...  

### pm2  

1. install

```shell
npm install pm2
```

2. auto start-up when power on  
```shell
pm2 startup
```

### frp  -- for intranet server

1. install

> https://github.com/fatedier/frp/releases  

```shell
wget https://github.com/fatedier/frp/releases/download/v0.36.2/frp_0.36.2_linux_amd64.tar.gz
tar -zxvf frp_0.36.2_linux_amd64.tar.gz
```

#### frps -- frp in server side  

1. delete file about client  
2. config frps.ini
> How to config ?  
> Coming soon...

#### frpc -- frp in client side  

1. delete file about server  
2. config frpc.ini
> How to config ?  
> Coming soon...



