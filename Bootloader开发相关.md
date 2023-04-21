# Bootloader开发相关



## 1、什么是BootLoader？

​		Bootloader是嵌入式系统在加电后执行的第一段代码，在它完成CPU和相关硬件的初始化之后，再将操作系统映像或固化的嵌入式应用程序装载到内存中然后跳转到操作系统所在的空间，启动操作系统运行。



我们先假设这样一个场景：车辆某个ECU只有Application Software，由于某种故障导致该ECU的Application Software异常，进而导致车辆故障，不能使用。既然属于Application Software问题，软件工程师修复好Application Software以后，重新将Application Software刷写进该ECU即可。问题来了：怎么将修复好的Application Software刷写进该ECU？

为了解决这个问题，Bootloader应运而生，即：Bootloader是为更新Application Software而存在。既然是为更新Application Software而存在，Bootloader就没有必要时常更新。<u>当车辆下线以后，Bootloader就固化在ECU指定内存区，不做更新，而Application Software可能会因用户的需求存在升级的可能。</u>



## 2、Bootloader如何更新App Software