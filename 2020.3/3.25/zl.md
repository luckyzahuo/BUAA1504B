> 2020/3/19 

## 1. C/C++ 基础知识
(1) C++程序中有哪些常见的内存泄露情况？

内存泄漏：指程序中已动态分配的**堆内存**由于某种原因程序未释放或无法释放，造成系统内存导致程序运行速度减慢甚至系统崩溃等严重后果。

1. 调用new后没有对应的delete。
2. 应该使用delete[]时使用了delete。
3. 没有将基类的虚构函数定义为虚函数。

## 2. 操作系统
(1) 线程同步与互斥的区别？

线程同步指的是多个线程相互协作关系，是一个比较大的概念。而线程互斥是指的多个线程对临界资源的独占使用。线程互斥可以看成是一种特殊的线程同步。


## 3. 计算机网络
(1) 什么是ARP，它的工作流程是怎样的？

地址解析协议，即 ARP(Address Resolution Protocol)，是根据IP地址获取物理地址的一个TCP/IP协议。

1. 主机A首先查看自己的ARP表，确认是否有主机B对应的ARP表项。如果找到了对应的MAC地址，则主机A直接利用ARP表中的MAC地址，对应IP地址进行帧封装，并将数据包发送给主机B。
2. 如果没有找到，就向本地网络发起一起ARP请求的广播包，查询目的主机对应的MAC地址。此ARP请求数据包里包括源主机的IP地址，硬件地址，以及目的主机的IP地址。
3. 网络中所有主机收到这个请求后，会检查数据包中的目的IP是否和自己的IP地址一致。如果不相同就忽略此数据包，如果相同，该主机首先将发送端的MAC地址和IP地址添加到自己的ARP列表中，如果ARP列表中已经存在该IP信息，则将其覆盖，然后给源主机发送一个ARP相应数据包，告诉对方自己是他需要查找的MAC地址，源主机收到这个ARP响应数据包后，将得到的目的主机的IP地址和MAC地址添加到自己的ARP列表中，并利用此信息开始数据传输。
4. 如果源主机一直没有收到ARP的相应数据包，则表示ARP查询失败。

## 4. 数据库
(1) 

## 5. 算法
(1) 最长回文子串

> 题目：给定一个字符串 s，找到 s 中最长的回文子串。

https://leetcode-cn.com/problems/longest-palindromic-substring/

```
```