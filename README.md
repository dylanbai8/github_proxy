# 为 Git 配置代理，改善 Github 国内 Push 速度

命令格式：
```
#设置 socks5 代理（本地DNS）
git config --global http.proxy socks5://your-server:your-port

#设置 socks5 代理（远程DNS）
git config --global http.proxy socks5h://your-server:your-port

#只对 github.com 代理
git config --global http.https://github.com.proxy socks5://your-server:your-port
```

# 以常用的 socks5本地 127.0.0.1:1080 为例
# 请先开启 ss ssr v2ray 等

设置全局代理
```
git config --global http.proxy socks5://127.0.0.1:1080
```

取消全局代理
```
git config --global --unset http.proxy
```

只对 github.com 代理
```
git config --global http.https://github.com.proxy socks5://127.0.0.1:1080
```

取消对 github.com 代理
```
git config --global --unset http.https://github.com.proxy
```

查看当前代理配置
```
git config --global -e
```
