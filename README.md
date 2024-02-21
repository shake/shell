记录一下梯子的过程

搬瓦工的vps，[官网]（https://bandwagonhost.com/）

[官网](https://github.com/jinwyp)

  bash <(curl -Lso- https://git.io/oneclick)

ubuntu 22.04，15选项。基本都是默认选项。没太多改动。

注册一个8块钱域名，这个域名，一年后需要更换，可以理解需要再次重装，需要看这个文档。

域名设置CF的dns服务器来解析。配置一下就可以。

整体速度不错。

如果面临速度问题，考虑所谓优选ip
[CloudflareSpeedTest](https://github.com/XIU2/CloudflareSpeedTest)

我测试，效果还是不错的。


eu.org 的二级域名，还没拿到，搞定以后就不需要折腾域名的事情。

后续提速，估计是需要使用优选ip。


[客户端](https://github.com/2dust) 。win11，6.33版本，
* 需要额外安装 [Microsoft .NET 6.0 Desktop Runtime](https://download.visualstudio.microsoft.com/download/pr/513d13b7-b456-45af-828b-b7b7981ff462/edf44a743b78f8b54a2cec97ce888346/windowsdesktop-runtime-6.0.15-win-x64.exe)
* [v2rayN-With-Core.zip] (https://github.com/2dust/v2rayN/releases/download/6.33/v2rayN-With-Core.zip)


# vps命令维护

## web

* Web服务器 nginx 安装成功! 伪装站点为 ai.xxx.site
* 伪装站点的静态html内容放置在目录 /nginxweb/html, 可自行更换网站内容.
* nginx 配置路径 /etc/nginx/nginx.conf
* nginx 访问日志 /nginxweb/nginx-access.log
* nginx 错误日志 /nginxweb/nginx-error.log
* nginx 查看日志命令: journalctl -n 50 -u nginx.service
* nginx 启动命令: systemctl start nginx.service
* nginx 停止命令: systemctl stop nginx.service
* nginx 重启命令: systemctl restart nginx.service
* nginx 查看运行状态命令: systemctl status nginx.service
  
  
  ## V2ray Version: 4.45.2 安装成功 !

  * V2ray 服务器端配置路径 /root/v2ray/config.json
  * V2ray 访问日志 /root/v2ray-access.log
  * V2ray 错误日志 /root/v2ray-error.log
  * V2ray 查看日志命令: journalctl -n 50 -u v2ray.service
  * V2ray 启动命令: systemctl start v2ray.service
  * V2ray 停止命令: systemctl stop v2ray.service
  * V2ray 重启命令: systemctl restart v2ray.service
  * V2ray 查看运行状态命令:  systemctl status v2ray.service



```
bash <(curl -Lso- https://git.io/oneclick)
 OS info: Ubuntu, ubuntu, 22.04, 22.04, jammy, intel CPU amd64, bash, apt-get, /lib/systemd/system/

 Trojan-go V2ray Xray 一键安装脚本 | 2024-2-3 | 系统支持：centos7+ / debian9+ / ubuntu16.04+


 1. 安装linux内核 bbr plus, 安装WireGuard, 用于解锁 Netflix 限制和避免弹出 Google reCAPTCHA 人机验证

 2. 安装 trojan/trojan-go 和 nginx, 支持CDN 开启websocket, trojan-go 运行在443端口
 3. 只安装 trojan/trojan-go 运行在443或自定义端口, 不安装nginx, 方便与现有网站或宝塔面板集成
 4. 卸载 trojan/trojan-go 和 nginx

 6. 安装 Shadowsocks Rust 支持 Shadowsocks 2022 加密方式, 运行在随机端口
 7. 安装 Xray Shadowsocks 支持 Shadowsocks 2022 加密方式, 运行在随机端口
 8. 卸载 Shadowsocks Rust 或 Xray 

 11. 安装 v2ray或xray 和 nginx ([Vmess/Vless]-[TCP/WS/gRPC/H2/QUIC]-TLS), 支持CDN, nginx 运行在443端口
 12. 只安装 v2ray或xray ([Vmess/Vless]-[TCP/WS/gRPC/H2/QUIC]), 无TLS加密, 方便与现有网站或宝塔面板集成

 13. 安装 v2ray或xray (VLess-TCP-[TLS/XTLS])+(VMess-TCP-TLS)+(VMess-WS-TLS) 支持CDN, 可选安装nginx, VLess运行在443端口
 14. 安装 v2ray或xray (VLess-gRPC-TLS) 支持CDN, 可选安装nginx, VLess运行在443端口
 15. 安装 v2ray或xray (VLess-TCP-[TLS/XTLS])+(VLess-WS-TLS) 支持CDN, 可选安装nginx, VLess运行在443端口
 16. 安装 v2ray或xray (VLess-TCP-[TLS/XTLS])+(VLess-WS-TLS)+xray自带的trojan, 支持CDN, 可选安装nginx, VLess运行在443端口
 17. 安装 v2ray或xray (VLess-TCP-XTLS Vision)) 不支持CDN, 可选安装nginx, VLess运行在443端口
 18. 安装 v2ray或xray (VLess-TCP-REALITY XTLS Vision)) 不支持CDN, 可选安装nginx, VLess运行在443端口
 19. 升级 v2ray或xray 到最新版本
 20. 卸载 v2ray或xray 和 nginx

 21. 同时安装 v2ray或xray 和 trojan-go (VLess-TCP-[TLS/XTLS])+(VLess-WS-TLS)+Trojan, 支持CDN, 可选安装nginx, VLess运行在443端口
 22. 同时安装 nginx, v2ray或xray 和 trojan-go (VLess/Vmess-WS-TLS)+Trojan, 支持CDN, trojan-go运行在443端口
 23. 同时安装 nginx, v2ray或xray 和 trojan-go, 通过 nginx SNI 分流, 支持CDN, 支持与现有网站共存, nginx 运行在443端口 
 24. 卸载 trojan-go, v2ray或xray 和 nginx

 25. 查看已安装的配置和用户密码等信息
 26. 申请免费的SSL证书
 30. 子菜单 安装 trojan 和 v2ray 可视化管理面板, VPS测速工具, Netflix测试解锁工具, 安装宝塔面板等
 ==================================================
 31. 安装DNS服务器 AdGuardHome 支持去广告
 32. 给 AdGuardHome 申请免费的SSL证书, 并开启DOH与DOT
 33. 安装DNS国内国外分流服务器 mosdns 或 mosdns-cn
 34. 卸载 mosdns 或 mosdns-cn DNS服务器 

 41. 安装OhMyZsh与插件zsh-autosuggestions, Micro编辑器 等软件
 42. 开启root用户SSH登陆, 如谷歌云默认关闭root登录,可以通过此项开启
 43. 修改SSH 登陆端口号
 44. 设置时区为北京时间
 45. 用 VI 编辑 authorized_keys 文件 填入公钥, 用于SSH免密码登录 增加安全性

 88. 升级脚本
 0. 退出脚本
```

我采用15选项，套接到cloudfire上。如果希望查看安装生成的信息，运行25就可以。
