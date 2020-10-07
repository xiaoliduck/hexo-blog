---
title: 自建DDNS
date: 2020-10-08 03:34:26
tags:
---
### 使用dynu.com的免費DDNS服務，建立您的DDNS。(dynu.com需要科學上網)


1. 打開下方鏈接登記您的帳戶

https://www.dynu.com/zh-CN/

然後進入「後台控制中心」

![0wELY6.jpg](https://s1.ax1x.com/2020/10/08/0wELY6.jpg)

![0wEjSO.jpg](https://s1.ax1x.com/2020/10/08/0wEjSO.jpg)

![0wEOfK.jpg](https://s1.ax1x.com/2020/10/08/0wEOfK.jpg)

![0wEHT1.jpg](https://s1.ax1x.com/2020/10/08/0wEHT1.jpg)

![0wEqFx.jpg](https://s1.ax1x.com/2020/10/08/0wEqFx.jpg)

2. 使用腳本讓VPS自動更新DDNS

登入您的VPS終端，執行下列命令
```
##Debian/Ubuntu
apt-get update
apt-get install curl -y

##CentOS
yum update -y
yum install 
```

```
curl "https://api.dynu.com/nic/update?hostname=您申請的域名&password=您Dynu帳戶的密碼"

## 返回下面信息表示成功 ##
good xxx.xxx.xxx.xxx (IP地址)
```
設定定時更新
```
crontab -e
```
按i进入编辑模式，貼上下方命令，並按esc一下，再输入:wq保存
```
*/1 * * * * curl "https://api.dynu.com/nic/update?hostname=您申請的域名&password=您Dynu帳戶的密碼"
 > /dev/null 2>&1

```
