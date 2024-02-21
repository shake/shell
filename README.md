记录一下梯子的过程

搬瓦工的vps，[官网]（https://bandwagonhost.com/）

[老大](https://github.com/jinwyp)

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


[客户端](https://github.com/2dust)


vps命令维护

* Web服务器 nginx 安装成功! 伪装站点为 ai.xxx.site
* 伪装站点的静态html内容放置在目录 /nginxweb/html, 可自行更换网站内容.

``
    nginx 配置路径 /etc/nginx/nginx.conf
    nginx 访问日志 /nginxweb/nginx-access.log
    nginx 错误日志 /nginxweb/nginx-error.log
    nginx 查看日志命令: journalctl -n 50 -u nginx.service
  ``
  nginx 启动命令: systemctl start nginx.service
  nginx 停止命令: systemctl stop nginx.service
  nginx 重启命令: systemctl restart nginx.service
  nginx 查看运行状态命令: systemctl status nginx.service
  
  
  V2ray Version: 4.45.2 安装成功 !
  V2ray 服务器端配置路径 /root/v2ray/config.json
  
  V2ray 访问日志 /root/v2ray-access.log
  V2ray 错误日志 /root/v2ray-error.log
  
  V2ray 查看日志命令: journalctl -n 50 -u v2ray.service
  
  V2ray 启动命令: systemctl start v2ray.service
  V2ray 停止命令: systemctl stop v2ray.service
  V2ray 重启命令: systemctl restart v2ray.service
  V2ray 查看运行状态命令:  systemctl status v2ray.service
