# Lab: Xv6 and Unix utilities

这个实验将带领大家熟悉xv6和它的系统调用，并通过xv6提供的系统调用来实现一些应用程序。

## 构建xv6操作系统

在命令行中执行指令`make qemu` ，会有一大堆的内容输出到屏幕，这些都是构建xv6过程中执行的相关命令。qemu会把构建好的xv6加载进虚拟机中，启动系统，输出一些初始化信息后，最后显示一个**$**提示符，你可以在这里输入命令，与xv6进行交互。那么xv6是如何一步步构建起来的呢？这就需要看看Makefile有些什么内容。

### Makefile

略，有空填

---



## sleep

1. 获得用户的输入参数sleep_time，使用atoi库函数将字符串参数转化为整形
2. 调用系统调用sleep，传入参数sleep_time
3. 调用系统调用exit，结束程序

### pingpong

1. 由于pipe的数据流是单向的，创建两个管道pfd1, pfd2，父进程用pfd1向子进程传递信息，子进程用pfd2向父进程传递信息
2. 调用fork，创建子进程
3. 父子进程关闭不使用的文件描述符
4. 
5. 运行结束

### primes

如何正确写出？

想清楚流程逻辑

谁给谁发送消息，何时发送结束，何时停止fork... 关闭文件描述符, 理解fork的时候什么是共享的



