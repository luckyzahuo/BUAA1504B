> 2020/3/19 

## 1. C/C++ 基础知识
(1) JVM在main方法执行之前，会有什么操作？

JVM 启动调用 main 方法，一共经过四个阶段：加载( Load )、链接( Linkage )、初始化( Initialization )、调用( Invocation )

## 2. 操作系统
(1) 为什么进程的上下文切换比线程上下文切换代价高？

当线程在同一个进程之中，一些资源是共享的，不用切换；而进程的切换需要一个进程运行所有的资源。

## 3. 计算机网络
(1) 什么是子网掩码？

一种用来指明一个IP地址的哪些位标识的是主机所在的子网，以及哪些位标识的是主机的位掩码。子网掩码不能单独存在，它必须结合IP地址一起使用。子网掩码只有一个作用，就是将某个IP地址划分成网络地址和主机地址两部分。

## 4. 数据库
(1) 视图的优缺点？

1、视图能够简化用户的操作  
2、视图使用户能以多钟角度看待同一数据  
3、视图对重构数据库提供了一定程度的逻辑独立性  
4、视图能够对机密数据提供安全保护  
5、适当的利用视图可以更清晰的表达查询  

## 5. 算法
(1) 整数反转

> 给出一个 32 位的有符号整数，你需要将这个整数中每位上的数字进行反转。https://leetcode-cn.com/problems/reverse-integer/

```c
int reverse(int x){
    long i = 0;
    long t = x;
    while(t)
    {
        i = 10*i + (t%10);
        t = t/10;
    }
    if(i < INT_MIN || i > INT_MAX)
    {
        return 0;
    }
    return i;
}

```