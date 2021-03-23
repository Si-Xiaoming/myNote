---
typora-root-url: image
---

# node.js

## 配置服务器

```javascript
//使用node做一个web服务器
//1.加载http核心模块
var http = require('http');
//2.使用http.createServer()创建一个web服务器
//返回一个Server实例
var server = http.createServer();
//3.服务器提供服务 发请求 接收请求 处理请求  给个反馈

//注册请求事件，就会触发服务器request请求事件，然后执行第二个参数，回调函数处理
server.on('request',function () {
    console.log("收到客户端请求！");
})

//4.绑定端口号   启动服务器
server.listen(3000,function () {
    console.log('succeed welcome to http://127.0.0.1:3000')
});
```

