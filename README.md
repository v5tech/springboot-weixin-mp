# springboot-weixin-mp

SpringBoot整合weixin-java-tools实现微信公众号登录授权

注册 `https://ngrok.com` 将本地服务端口代理映射到公网，微信服务器端绑定映射到ngrok的域名进行调试

```bash
wget https://bin.equinox.io/c/4VmDzA7iaHb/ngrok-stable-windows-amd64.zip

unzip ngrok-stable-windows-amd64.zip

ngrok authtoken 8TAZn4p5inht6MUKtkPzJ_6Amr8yEUYu6ZBndQ2CCKS

ngrok http 8080

ngrok by @inconshreveable                                                                               (Ctrl+C to quit)

Session Status                online
Account                       冯靖 (Plan: Free)                                                                         Fo
rsion                       2.3.27                                                                                    Re
gion                        United States (us)                                                                        We
b Interface                 http://127.0.0.1:4040
Forwarding                    http://441aca54.ngrok.io -> http://localhost:8080
Forwarding                    https://441aca54.ngrok.io -> http://localhost:8080

Connections                   ttl     opn     rt1     rt5     p50     p90
                              0       0       0.00    0.00    0.00    0.00
```

启动项目，将本地8080代理到441aca54.ngrok.io的80端口，在微信服务器端设置该域名后访问`https://441aca54.ngrok.io/wechat/authorize?returnUrl=http://baidu.com`即可获取微信用户信息

参考项目

https://github.com/wechat-group/WxJava

https://github.com/binarywang/weixin-java-mp-demo-springboot
