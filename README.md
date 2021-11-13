# 计算机网络实验

计算机网络课程实验一共有四个，持续五周，其中实验 1 安排两周完成。

- 实验 1 - IP 组网
- 实验 2 - TCP/UDP 通信程序设计
- 实验 3 - RDT 通信程序设计
- 实验 4 - Internet 应用实例分析



## 实验环境的安装

这一部分是为想在自己电脑上做的同学准备的。

### Ubuntu

实验中心的 Linux 环境是 Ubuntu 18.04，所以这里以 Ubuntu 为例解释。自己安装可以选择更新的版本，有兴趣挑战的同学也可以试试其它发行版，例如 Arch、Manjaro。

安装好之后建议换源，提升软件下载速度，可以选择[科大源](https://mirrors.ustc.edu.cn/help/ubuntu.html)。

换源后需要更新系统并安装实验需要的程序，如下：

```shell
sudo apt update
sudo apt install -y vim traceroute build-essential curl tcpdump wireshark
sudo snap install --classic code

# 20.04之前的版本中，建议安装这个字体
sudo apt install -y fonts-droid
```



### Packet Tracer

实验中心的 Packet Tracer 是安装在 Windows 系统中的，同学自己使用可以装在 Ubuntu 中，要求版本不低于 20.04。Ubuntu 的 Packet Tracer 的安装包可以在[这里](https://ia801801.us.archive.org/29/items/packet-tracer-800-build-212-mac-notarized/PacketTracer_800_amd64_build212_final.deb)下载。

```shell
#安装deb包
sudo apt install -y PacketTracer_800_amd64_build212_final.deb
#启动PacketTracer，使用unshare阻止联网，实现免登陆
sudo LD_LIBRARY_PATH=/opt/pt/bin:$LD_LIBRARY_PATH unshare -n /opt/pt/bin/PacketTracer --no-sandbox
```

Windows 的 Packet Tracer 的安装包可以在[这里](https://ia801801.us.archive.org/29/items/packet-tracer-800-build-212-mac-notarized/PacketTracer800_Build212_64bit_setup-signed.exe)下载。
