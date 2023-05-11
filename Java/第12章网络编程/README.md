# 第12章 网络编程

网络编程顾名思义就是编写能够进行网络数据交互的应用程序。

> **网络编程三要素**

在学习网络编程之前我们必须了解一些有关网络的一些关键词。

```java
【ip地址】
	ip地址用来标识网络中的一台主机，在同一个局域网中ip地址不能重复。
	分为ipv4和ipv6
        - IpV4:  4个字节      4*8=32位
            如：192.168.1.11

        - IpV6： 16个字节      16*8=128位
    		如：fe80::2ca8:cc7e:bef0:a1cf%12
                
     注意：如果自己的电脑没有连接互联网或者局域网，
     可以使用127.0.0.1地址用于测试学习，这个地址可以用于本机和本机进行通讯。
                
【端口号】
    表示一台主机上的某一个程序，用一个整数表示

【网络协议】
    表示在网络中数据通信的规则
    UDP: 面向无连接的，不可靠的网络协议，效率高
    TCP: 面向有连接，可靠的网络协议，效率低
```

> **InetAddress类**

先学习一个表示IP地址的类InetAddress，该类中提供了一些方法用于获取主机名或者主机地址。

```java
public static InetAddress getByName(String host)  
    根据主机名或者ip地址，获取InetAddress对象
public String getHostAddress()
    获取主机ip地址
public String getHostName()
    获取主机名称
```

演示上面方法的使用

```java
public class InetAddressDemo {
    public static void main(String[] args){
        //获取InetAddress对象
        InetAddress address = InetAddress.getByName("192.168.31.130");
        System.out.println(address);

        //获取ip地址
        String hostAddress = address.getHostAddress();
        System.out.println(hostAddress);
        //获取主机名
        String hostName = address.getHostName();
        System.out.println(hostName);
    }
}
```





