# linux 基本操作

## ssh 超时自动断开链接怎么办 ？
修改 `server` 端的 `/etc/ssh/sshd_config` 文件：`vim /etc/ssh/sshd_config`  
```bash
ClientAliveInterval 60 ＃server每隔60秒发送一次请求给client，然后client响应，从而保持连接  
ClientAliveCountMax 3 ＃server发出请求后，客户端没有响应得次数达到3，就自动断开连接，正常情况下，client不会不响应。
```
