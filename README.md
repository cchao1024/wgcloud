<p align="center">
  <a  target="_blank" href="http://www.wgstart.com">
    <img src="./demo/logo.png">
  </a>
 </p>



## WGCLOUD介绍

WGCLOUD设计思想为新一代极简运维监控系统，提倡快速部署，降低运维学习难度，全自动化运行，无模板和脚本。**当前仓库版本为v2.3.7最新，git拉取master分支即可**。

[**【2021.12.10 重要公告】关于Apache Log4j 远程代码执行漏洞对WGCLOUD无影响的说明**](https://www.cnblogs.com/wanghouhou/p/15671567.html)

WGCLOUD基于微服务springboot架构开发，是轻量高性能的分布式监控系统，核心采集指标包括：**主机系统信息，网络流量，CPU状态，CPU温度，内存状态，磁盘空间和IO监控，硬盘smart健康检测，系统负载，大屏可视化，ES集群状态，数据可视化监控(mysql，oracle，pgsql等)，服务接口检测，应用进程监控，网络拓扑图，端口监控，日志文件监控，docker监控，文件防篡改保护，数通设备监测，Web SSH，堡垒机，指令批量下发，告警信息（邮件微信钉钉短信等）推送**。[english readme](<./README_en.md>)

1.v2.3.7放弃了v2.3.6版本的sigar方式获取主机指标，v2.3.7采用流行的OSHI组件来采集主机指标

2.采用服务端和客户端协同工作方式，更轻量，更高效，可支持数千台主机同时在线监控。

3.server端负责接受数据，处理数据，生成图表展示。agent端默认每隔2分钟(时间可调)上报主机指标数据。

4.支持主流服务器平台安装部署，如Linux, Windows,macOS,Unix等。

5.WGCLOUD采用springboot+bootstrap，完美实现了分布式监控系统，为反哺开源社区，二次开源。

6.当前仓库为开源版，v3为商业版（免费），**生产环境建议部署商业版**，商业版功能、性能更优秀，请点击查看[开源版和商业版区别](<./开源版和商业版区别.md>)

7.如果你觉得WGCLOUD帮助到了你，不用打赏我们，只要点击star支持下就好了。

## **网站**

<http://www.wgstart.com>

## **Github仓库(2.8k⭐)**

<https://github.com/tianshiyeben/wgcloud>

## **视频**

B站WGCLOUD相关视频地址，<https://space.bilibili.com/549621501/video>

## **源码使用**

1.使用IDEA的话（推荐），直接打开wgcloud-server和wgcloud-agent即可，JDK使用1.8

2.使用Eclipse的话，导入maven工程wgcloud-server和wgcloud-agent即可，JDK使用1.8

3.运行所需sql脚本（本项目使用mysql数据库），在sql文件夹下，在mysql数据库里创建数据库wgcloud，导入wgcloud.sql即可

4.bin目录下的脚本文件，为server启动脚本（linux和windows），和打包好的wgcloud-server-release.jar放到同一个目录下即可。agent启动脚本仿照server稍微修改下即可。

## **功能截图**



![WGCLOUD监控主面板](./demo/demo2.jpg)

![WGCLOUD监控主机列表](./demo/demo3.jpg)

![WGCLOUD监控主机列表](./demo/report.jpg)

![WGCLOUD监控主机列表](./demo/dp.jpg)

![WGCLOUD监控图表](./demo/demo4.jpg)



![WGCLOUD网络拓扑图](./demo/tpdemo.jpg)

![WGCLOUD主机web ssh客户端图](./demo/ssh.jpg)

![WGCLOUD主机画像图](./demo/huaxiang.jpg)


## 运行环境

1.JDK1.8

2.mysql5.6及以上

3.支持操作系统平台

> 支持监测Linux系列：Debian、RedHat、CentOS、ubuntu、麒麟、统信、龙芯、树莓派等
> 支持监测windows系列：Windows Server 2008 R2，2012，2016，2019，Windows 7，Windows 8，Windows 10
> 支持监测unix系列：solaris，FreeBSD，OpenBSD
> 支持监测macOS系列：macOS amd64



## 联系

邮箱：tianshiyeben@qq.com

## 感谢

JetBrains提供的免费license