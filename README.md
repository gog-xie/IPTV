<h1 align="center"> 🏦IPTV单线复用内网融合组播转单播</h1>

## 适用范围
> * ***本项目适用于四川地区家庭IPTV内网融合组播转单播，不同地区仅单播IP地址的第三位不相同，可自行找规律。***

## 搭建过程
> * ***由于家庭内网IPTV占用带宽流量普通高清通常在10Mbps以下，4K高清通常在30Mbps以下，对于家庭带宽通常为1000M，对于多设备同时观看IPTV对上网带宽几乎影响很小，故本项目仅介绍单线复用。***
- ### 1、光猫设置
  通常建议光猫桥接，路由器拨号。
光猫设置分为两种情况，华为光猫和中兴光猫略有不同：华为光猫不用绑定网口均带有Internet和ITV业务数据，而中兴光猫需绑定Internet和ITV业务数据，如光猫Lan1需勾选上网和ITV业务数据，则Lan1带了两种业务数据。
- ### 2、路由器设置
  路由器可选用小米、华硕、OpenWrt等路由器，在主路由上实现IPTV内网融合，也可在旁路由上实现，通常旁路由以PVE、NAS等为载体，时有关机的可能，而主路由几乎24小时开机，故部署在主路由上为佳，本项目以华硕路由器为主路由为例。
- ### 3、数据抓包
  采用一台双网口电脑，将两个网口桥接，一个网口接光猫ITV数据，一个网口接电信机顶盒，电脑安装Wireshark软件，并选择两个网口中的一个，开始抓包，开启机顶盒，并进入直播，换台、移时观看、点播，停止抓包。抓包数据http数据追踪流HTTP数据，保存数据上传到[IPTV数据解析工具](https://gyssi.link/iptv/888.html) 生成m3u文件，再将播放地址配合内网地址修改为http://内网地址:端口号/udp/电视台地址:电视台端口号，如http://192.168.50.1:5555/udp/239.94.1.147:5140，修改后，再上传[自动匹配生成带有台标m3u文件](https://epg.51zmt.top:8001)
- ### 4、播放
  播放软件通常采用Kodi、PotPlayer等。电视端用Kodi比较适合，开机进入电视播放，需安装IPTV Simple Client插件，进入插件设置，添加附加配置，名称随便填，位置填“远程路径（互联网地址）”，M3U播放列表URL填入以下IPTV节目列表地址即可。

## IPTV节目列表
> ### [Github地址：](https://raw.githubusercontent.com/gog-xie/IPTV/refs/heads/main/MTU_Address/202509.m3u)

```
https://raw.githubusercontent.com/gog-xie/IPTV/refs/heads/main/MTU_Address/202509.m3u
```

> ### [镜像地址：](https://fastly.jsdelivr.net/gh/gog-xie/IPTV@main/MTU_Address/202509.m3u)

```
https://fastly.jsdelivr.net/gh/gog-xie/IPTV@main/MTU_Address/202509.m3u
```
