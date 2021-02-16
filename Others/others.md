Number的存储空间是多大，如何解决？
-------------
js的number类型有个最大值（安全值），即2的53次方。如果超过了这个值，js就会出现不精准的问题。<br/>
1）后端发字符串类型
将后端发过来的long类型转为string类型再向前端传参。但若是传的是DAO集合（数据访问对象是一个面向对象的数据库接口），则需对每个转类型，太过繁琐。

fetch API与传统request的区别
---------------
fetch 是浏览器提供的一个新的 web API，它用来代替 Ajax（XMLHttpRequest），其提供了更优雅的接口，更灵活强大的功能。fetch API 提供了对请求更精确的控制。对 cookie，对跨域等功能都有了传统 Ajax（XMLHttpRequest）没有的功能，响应（response）还提供了一些的原来没有的标志位。

websocket与ajax的区别
-----------------
1）本质不同<br/>
Ajax,即异步JavaScript和XML，是一种创建交互式网页应用的网页开发技术；WebSocket是HTML5一种新的协议，实现了浏览器与服务器全双工通信。其本质是先通过HTTP/HTTPS协议进行握手后创建一个用于交换数据的TCP连接，服务端与客户端通过此TCP连接进行实时通信。<br/>
2）生命周期不同<br/>
websocket建立的是长连接，在一个会话中一直保持连接；而ajax是短连接，数据发送和接受完成后就会断开连接。<br/>
3）适用范围不同<br/>
websocket一般用于前后端实时数据交互，而ajax前后端非实时数据交互。<br/>
4）发起人不同<br/>
Ajax技术需要客户端发起请求，而WebSocket服务器和客户端可以相互推送信息。<br/>
5）用法不同<br/>
```
ajax：
  $.ajax({
    type:"post",
    url:"http://localhost:8080/target",
    data:"state = yes",
    dataType:"json",
    success:funciont(data){
    }
  });
 
websocket:
  var monitor = new WebSocket("ws://"+ip+path)
  onOpen()、onMessage()、onClose()
```
[详情请点击](https://blog.csdn.net/qiuhuanmin/article/details/50719114)


