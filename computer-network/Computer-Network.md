## 计算机网络部分常见知识

````text
如有错误之处，敬请指教。
````


### OSI七层模型
>OSI(Open System Interconnect开放式系统互联)。

**它是ISO(国际标准化组织)提出的网络互联模型。
OSI模型定义了网络互联的7层框架:
应用层，表示层，会话层，传输层，网络层，数据链路层，物理层。**

![OSI7层模型](../img/OSI%207层模型.png)

#### OSI网络互联模型为什么要分层?
>分层可以把开放系统中信息交换的问题分解到具体的层级之中，
>而各层可以对各自的功能独自做出修改和扩展，体现了解耦的思想。

1.物理层
>物理层的作用是利用光纤，电缆，双绞线等传输介质来传输比特流(光，电等信号)。
>需要ISP(Internet Service Provider)互联网提供商的支持。

2.链路层
>链路层的作用是当网络层数据传输前，将数据封装成帧。
>一个帧由一个数据字段和若干首部字段组成，网络层的数据报就存于数据字段中。
>当帧中的数据作为bit传输时，
>接收方可能会判断错误，如0判断成1。
>这种错误是由于在数据发送过程中外部因素如电磁噪声干扰所致，
>许多链路层协议就提供了一种纠错机制，通过让发送节点在帧中包括差错bit，
>让接受节点进行差错检查。

3.网络层
>网络层主要负责数据的数据链路的寻址和路由选择。
>网络层的协议主要有:IP,ICMP等。

4.传输层
>传输层提供端口到端口的可靠的数据传输服务。传输层的协议主要有TCP和UDP。

5.会话层
>会话层的作用是负责建立，管理和终止主机之间的通信连接。

6.表示层
>表示层主要的作用是负责数据格式的转换:
>将应用层的数据转换为网络传输的格式，
>或者将来自下一层的数据转为应用层协议能够处理的格式。
>除此之外，数据的压缩解压，加密解密也都由表示层完成。

7.应用层
>应用层为应用程序提供SPI(Service Provider Interface)应用程序接口。
>应用层协议是为应用程序提供服务保证的协议。

### TCP/IP
>TCP / IP 不仅仅是指TCP和IP这两种协议，而是一系列网络协议的总和，
>而这些协议中最核心的2个协议就是TCP和IP，所以被称为TCP/IP网络协议族。
>TCP/IP协议族是互联网的基础通信架构。