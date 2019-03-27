# 为 Github 添加代理，改善国内 Push 速度。

命令格式：
```
http代理
git config --global http.proxy http://your-server:your-port

sock5代理
git config --global http.proxy socks5://your-server:your-port

sock5代理 远端DNS
git config --global http.proxy socks5h://your-server:your-port

只代理指定网站
git config --global http.https://github.com.proxy socks5://your-server:your-port
```

# 已常用的 sock5为例 （ ss ssr v2ray 等）

全局代理
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
git config --global --unset http.https://github.com.proxy)
```

查看当前代理配置
```
git config --global -e
``



