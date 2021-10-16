# v2ray-agent


* * *


## 支持的安装类型

- VLESS+TCP+TLS
- VLESS+TCP+xtls-rprx-direct【**推荐**】
- VLESS+gRPC+TLS【支持CDN、IPv6、延迟低】
- VLESS+WS+TLS【支持CDN、IPv6】
- Trojan+TCP+TLS【**推荐**】
- Trojan+TCP+xtls-rprx-direct【**推荐**】
- Trojan+gRPC+TLS【支持CDN、IPv6、延迟低】
- VMess+WS+TLS【支持CDN、IPv6】


## 线路推荐

- 1.GIA
- 2.上海CN2+HK
- 3.上海联通+台湾TFN
- 4.上海联通+Vultr东京
- 5.广移/珠移+HKIX/CMI/NTT
- 6.苏日IPLC+日本/美国
- 7.莞港IPLC+HK
- 8.广移/CN2+Cloudflare+全球
- 9.广移/CN2/南联+香港AZ+全球
- 10.北联+西伯利亚、伯力ttk/RT
- 11.CN2+HE
- 12.电信+台湾远传电信
- 13.CN2+JP NTT
- 14.中转+cloudflare+落地机【可拉全球】

## 组合推荐

- 中转/gia ---> VLESS+TCP+TLS/XTLS、Trojan【推荐使用XTLS的xtls-rprx-direct】
- 移动宽带 ---> VMESS+WS+TLS/VLESS+WS+TLS/VLESS+gRPC+TLS/Trojan+gRPC+TLS + Cloudflare
- cloudflare-> VLESS+gRPC+TLS/Trojan+gRPC+TLS[多路复用、延迟低]

## 注意事项

- **修改Cloudflare->SSL/TLS->Overview->Full**
- **Cloudflare ---> A记录解析的云朵必须为灰色【如非灰色，会影响到定时任务自动续签证书】**
- **使用纯净系统安装，如使用其他脚本安装过，请重新build系统再安装**
- wget: command not found [**这里需要自己手动安装下wget**]
  ，如未使用过Linux，[点击查看](https://github.com/mack-a/v2ray-agent/tree/master/documents/install_tools.md)安装教程
- 不支持非root账户
- **中间的版本号升级意味可能不兼容之前安装的内容，如果不是追新用户或者必须升级的版本请谨慎升级。** 例如 2.2.\*，不兼容2.1.\*
- **如发现Nginx相关问题，请卸载掉自编译的nginx或者重新build系统**
- **为了节约时间，反馈请带上详细截图或者按照模版规范，无截图或者不按照规范的issue会被直接关闭**
- **不建议GCP用户使用**
- **不建议使用Centos以及低版本的系统，如果Centos安装失败，请切换至Debian10重新尝试，脚本不再支持Centos6、Ubuntu 16.x**
- **[如有使用不明白的地方请先查看脚本使用指南](https://github.com/mack-a/v2ray-agent/blob/master/documents/how_to_use.md)**
- **Oracle vps有一个额外的防火墙，需要手动设置**
- **如果使用gRPC通过cloudflare转发,需要在cloudflare设置允许gRPC，cloudflare Network->gRPC**
- **gRPC目前处于测试阶段，可能对你使用的客户端不兼容，如不能使用请忽略**
- **低版本脚本升级高版本时无法启动问题，[请点击此链接查看解决方案](https://github.com/mack-a/v2ray-agent/blob/master/documents/how_to_use.md#4%E4%BD%8E%E7%89%88%E6%9C%AC%E5%8D%87%E7%BA%A7%E9%AB%98%E7%89%88%E6%9C%AC%E5%90%8E%E6%97%A0%E6%B3%95%E5%90%AF%E5%8A%A8%E6%A0%B8%E5%BF%83)**

## [脚本使用指南](https://github.com/mack-a/v2ray-agent/blob/master/documents/how_to_use.md)、[脚本目录](https://github.com/mack-a/v2ray-agent/blob/master/documents/how_to_use.md#5脚本目录)
  
## 安装脚本

- 支持快捷方式启动，安装完毕后，shell输入【**vasma**】即可打开脚本，脚本执行路径[**/etc/v2ray-agent/install.sh**]

- Latest Version【推荐】

```
wget -N --no-check-certificate "https://raw.githubusercontent.com/mack-a/v2ray-agent/master/install.sh" && chmod 700 install.sh && ./install.sh
```

# 示例图

<img src="https://raw.githubusercontent.com/mack-a/v2ray-agent/master/fodder/install/install.jpg" width=700>

# 许可证

[GPL-3.0](https://github.com/mack-a/v2ray-agent/blob/master/LICENSE)

## Stargazers over time

[![Stargazers over time](https://starchart.cc/mack-a/v2ray-agent.svg)](https://starchart.cc/mack-a/v2ray-agent)
