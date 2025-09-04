<h1 align="center"> 🏦单线复用IPTV内网融合组播转单播</h1>

## 适用范围
> * **本项目适用于四川地区家庭IPTV内网融合组播转单播，不同地区仅单播IP地址的第三位不相同，可自行找规律。**

## 搭建要求
> * ***由于家庭内网IPTV占用带宽流量普通高清通常在10Mbps以下，4K高清通常在30Mbps以下，对于家庭带宽通常为1000M，对于多设备观看IPTV对上网带宽几乎影响很小，故本项目介绍单线复用。***
- ### 1、光猫设置
通常建议光猫桥接，路由器拨号。
光猫设置分为两种情况，华为光猫和中兴光猫略有不同：
华为光猫不用绑定网口均带有Internet和ITV业务数据，而中兴光猫需绑定
- ### 2、路由器设置
路由器可用小米、华硕、OpenWrt等作为主路由，在主路由上实现IPTV内网融合，也可在旁路由上实现，旁路由以PVE、NAS等为载体，时有关机的可能，而主路由几乎24小时开机，故部署在主路由上为佳，本项目以华硕路由器为主路由为例。
- ### 3、数据抓包
采用一台双网口电脑，

## 四川电信IPTV节目列表
> ### [Github地址：](https://raw.githubusercontent.com/gog-xie/IPTV/refs/heads/main/MTU_Address/202509.m3u)

```
https://raw.githubusercontent.com/gog-xie/IPTV/refs/heads/main/MTU_Address/202509.m3u
```

> ### [镜像地址：](https://fastly.jsdelivr.net/gh/gog-xie/IPTV@main/MTU_Address/202509.m3u)

```
https://fastly.jsdelivr.net/gh/gog-xie/IPTV@main/MTU_Address/202509.m3u
```
