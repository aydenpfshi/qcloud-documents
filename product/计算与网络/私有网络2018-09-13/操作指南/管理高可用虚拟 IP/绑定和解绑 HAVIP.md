HAVIP 不是在腾讯云的控制台绑定，而是配合第三方 HA 软件使用。您需要在第三方 HA 软件中操作，将 HAVIP 指定为可漂移的 VIP 即可。然后由第三方 HA 软件通过 ARP 协议指定 HAVIP 要绑定的网卡。示意图如下，具体操作请参见第三方 HA 软件：
![](https://main.qcloudimg.com/raw/c2e4c1e75b972cb030cc9b6a4c8613e3.png)
传统物理设备环境下，所有内网 IP 默认都是可以通过 ARP 协议绑定到网卡上的，都可以在 HA 软件中指定为可漂移的 IP。
>?公有云环境下普通内网 IP 禁止了 ARP 协议，在 HA 软件中指定为可漂移 IP 的话，会导致漂移失败。

在此过程中：
1. HAVIP 只是被操作的对象，作为可被声明绑定的内网IP。操作的发起方为第三方 HA 软件，不在 HAVIP 的控制台实现绑定和解绑。
2. 操作时云服务器内的 HA 软件中，将 HAVIP 指定为可漂移的 VIP。此操作与第三方 HA 软件在非云平台的操作完全一样，不同 HA 软件的操作请参见该软件的操作指南（常见的 HA 软件有：Linux 下的 HeartBeat、keepalived、pacemaker，Windows下的 MSCS 等）。
操作示例：HA 软件中指定 VIP 时（配置文件或操作界面均可），填入您创建的 HAVIP 即可，如下图：
![](https://main.qcloudimg.com/raw/e43ccc658badc6d11c59793639233d76.png)
