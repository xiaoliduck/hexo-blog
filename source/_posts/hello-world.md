---
title: Hello World
---

### proxy settings

```
git config --global --unset https.proxy 
git config --global --unset http.proxy
```

### 变量设置
```
export PATH=$PATH:$HOME/bin:/sbin:/usr/bin:/usr/sbin
```
### 修改DNS
```
sudo vi /etc/resolv.conf
nameserver 114.114.114.114
nameserver 8.8.8.8
nameserver 8.8.4.4
nameserver 1.1.1.1
```
### 关闭centos防火墙
```
systemctl stop firewalld.service
systemctl disable firewalld.service
```
