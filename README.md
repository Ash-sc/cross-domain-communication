# 网页跨域通信前端解决方案Demo

> How to work ？

> 想要在本地运行该demo，你需要按照如下步骤：

### 1. 设置本机host

  首先设置本机本机host如下:

```
127.0.0.1        localhost
127.0.0.1        eg1.example.com
127.0.0.1        eg2.example.com
127.0.0.1        eg1.example-1.com
127.0.0.1        eg2.example-1.com
```

### 2. 设置静态服务

  设置静态服务以保证 http://localhost/ 指向 cross-domain-communication 项目文件夹

  以下是使用Nginx设置的示例：

```
    # 跨域通信示例
    server {
        listen       80;
        server_name  localhost;
        client_max_body_size    100m;

        location / {
            root /*******你本地的路径*******/cross-domain-communication/;
            try_files $uri $uri/ /index.html;
        }
    }
```

### 当然，你也可以直接查看线上示例


  [http://eg1.2017017.xyz/cdc/](http://eg1.2017017.xyz/cdc/)
