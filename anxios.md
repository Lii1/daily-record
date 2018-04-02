# anxios的使用

*记录疑问和一些需要注意的点: what why how when where*

怕是要系统学习一番哦

## 主要知识点

 

## HTTP

	### http请求方法



1. HEAD（响应GET的响应，但不包括响应体）,PUT（增量替换）,DELETE（删除指定资源）,OPTIONS（用于客户端查看服务端的性能，支持哪些方法和头部信息，一般是预检请求会用到）  这几种方法的发送和get和post一样吗？

	### momp-fe项目中的anxios封装http请求



* get,post,mock,http,reject

* 没有封装取消请求的函数

  ###anxios简介

  ​

1. `withCredentials: true`  设置是否跨域，默认为false
2. `navigator.sendBeacon(HttpRoot + url, postData)` 通过HTTP将少量的数据异步传输到服务器。主要可用于`统计和诊断代码`，在页面卸载前进行数据的传输