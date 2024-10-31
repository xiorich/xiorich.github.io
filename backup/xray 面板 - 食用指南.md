支持多协议多用户的 xray 面板 适配Alpine linux 使用F大编译的x-ui 支持的协议：vmess、vless、trojan、shadowsocks、dokodemo-door、socks、http 默认端口可使用x-ui命令更换 ovz，lxc虚拟化的vps，在纯净系统首次安装后内存占用约为27m左右，重启后内存占用约为20m

[![](https://camo.githubusercontent.com/a7699c0b9a644e656f297368579f11324544581b279e2684c35a90fb56835ff0/68747470733a2f2f706963322e7a697975616e2e77616e672f757365722f3077302f323032342f30382f72692532305f315f5f643535396535616238393730312e6a70673f7261773d74727565) ](我身处俗世 昨日如观花)

 _**需要注意的一点是，并不是所有的服务器都支持部署。**_

 VPN指的是代理服务器，也就是网民俗称的“翻墙软件”，而它要翻的那个墙就是“防火墙”。防火墙是中国实现互联网管理一整套技术系统的民间叫法，官方在正式场合从不这么叫它。
 
 防火墙并非是把中国互联网同境外互联网隔开，而是对境外个别网站及具体网页施行定点屏蔽。网络与网络是通的，但中国网络与境外网络个别点的联系受到拦截。需要指出的是，在境外互联网的浩瀚海洋中，这些被拦截点加起来只占很少的部分。

由于有的被屏蔽网站和网页在中国部分网民中很有影响，比如谷歌、脸谱、推特等是美国的主流网站，因此在国内外都有人把对它们的屏蔽看得很重。西方舆论一直把这件事当成中国“没有网络自由”的突出例证。

然而对于没兴趣上这些被屏蔽网站的人来说，这个问题又几乎不存在。实际情形是，这两种感受都在各自的方向上不断深化或扩大。
 
如果我们跳出是非的争论，来看中国互联网发展的总体面貌，那么会有一些有趣的发现。它们是，中国的防火墙实际上已经“成功”，造就了中国今天互联网发展的基本现实。比如中国出现了BAT这样的网络巨头，它们满足了中国网民的绝大多数需求，并得以向境外扩张。这或许是防火墙的“意外成果”，因为如果没有它和相应的其他管理，中国今天说不定会是“谷歌中国”、“雅虎中国”、“脸谱中国”的天下。

**安装工具**

1、[安装finalshell](https://www.hostbuf.com/t/988.html)

 2、安装X-UI面板

3、[安装v2ray](https://github.com/2dust/v2rayN/releases)

 ### 使用代码
 1、开启防火墙
 
 ```css
 iptables -P INPUT ACCEPT
 iptables -P FORWARD ACCEPT
 iptables -P OUTPUT ACCEPT
 iptables -F
 apt-get purge netfilter-persistent
```
 
 输入reboot，重启服务器
 
 ```css
一键安装依赖包（可用可不用）
 
 Debian/Ubuntu系统：apt update -y&&apt install -y curl&&apt install -y socat
 CentOS系统：yum update -y&&yum install -y curl&&yum install -y socat
 ```
 
 ```css
 2、申请SSL证书
 
 apt update -y       # Debian/Ubuntu 命令
 apt install -y curl   # Debian/Ubuntu 命令
 apt install -y socat  # Debian/Ubuntu 命令
 
 yum update -y        #CentOS 命令
 yum install -y curl    #CentOS 命令
 yum install -y socat   #CentOS 命令
 ```

 ```css
 Debian 系统上，cron 是默认安装的。但是，如果您的计算机上未安装它，请使用 root 权限在终端上运行以下几个命令。

 apt-get update

 apt-get install cron
 ```
 
 ```css
 3、开始申请证书
 
 curl https://get.acme.sh | sh
 
 ~/.acme.sh/acme.sh --register-account -m example@xx.com（替换成自己的邮箱）
 
 ~/.acme.sh/acme.sh --issue -d 域名 --standalone   
 #替换成自己解析好的域名，注意前后要有空格
 ```
 
 ```css
 4、安装证书
 
 ~/.acme.sh/acme.sh --installcert -d 域名 --key-file /root/private.key --fullchain-file /root/cert.crt    
#部分替换成自己解析好的域名，注意前后要有空格
 #刷新Fianlshell窗口，在root目录下可看到证书公钥/root/cert.crt及验证文件/root/private.ke
 ```
 
 ```css
 5、安装Xray面板，项目地址：【[点击进入](https://github.com/vaxilu/x-ui)】
 
 bash <(curl -Ls https://raw.githubusercontent.com/vaxilu/x-ui/master/install.sh)
 ```
 
 ```css
7、BBR加速，项目地址：【[点击进入](https://github.com/Chikage0o0/Linux-NetSpeed)】

 wget -N --no-check-certificate "https://raw.githubusercontent.com/chiakge/Linux-NetSpeed/master/tcp.sh" && chmod +x tcp.sh && ./tcp.sh
 ```

6、如果打不开v2rayN.exe,可以安装[.NET Framework 4.8](https://dotnet.microsoft.com/download/dotnet-framework/net48)

 下载链接：https://docs.microsoft.com/zh-cn/dotnet/framework/install/guide-for-developers

