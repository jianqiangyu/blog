---
title: DNS协议
date: 2021-05-30 18:59:26
tags: 网络协议 DNS
---

## 简介
由于ip地址不方便记忆,并且不能表达组织的名称和特点,所以人们设计出了域名(jd.com)
由于域名的不定长, 耗费字节更多, 路由器更喜欢定长, 有层次结构的IP地址.所以,在实际的网络连接中,还是需要知道目标主机的IP地址.
所以DNS(Domain Name System)出现了, 他可以根据域名找到对应IP地址


## DNS工作机制
为了方便将一个域名转换成一个IP地址, 
最简单的方式是只使用一个DNS服务器, 该服务器包含所有映射
但是这种方式, 存在一些问题: 
1. 单点故障: 该服务器出现故障, 整个互联网都无法正常使用
2. 位置: 一台服务器不可能离所有主机都近,如果距离过远,将会导致极大的时延
3. 维护: 一台服务器存放了所有数据, 将导致这个中央数据库过大,而且需要频繁更新, 另一方面, 这个服务器需要跟所有主机建立连接,处理查询

所以DNS采用了分布式的设计方案, 使用了大量的服务器, 根据级别不同,  以层次方式组织, 分布在世界各处

DNS服务器类型:
1. 根DNS服务器
2. 顶级域DNS服务器 
通用顶级域名(.com / .net  / .org / .edu / .gov/ .int)
国家及地区顶级域名(.cn / .jp / .uk)
新通用顶级域名(.vip / .xyz / .top / .club / .shop)
3. 权威DNS服务器

git clone --recurse-submodules "ssh://wangyubj06@gerrit.zhenguanyu.com:29418/aries-ios" && scp -p -P 29418 wangyubj06@gerrit.zhenguanyu.com:hooks/commit-msg "aries-ios/.git/hooks/"
