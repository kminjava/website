---
title: http请求网关
keywords: soul
description: http请求网关
---


## 说明

* 本篇文章主要是说明，http用户如何对网关进行请求。

* 请求之前，请确保你启动了 `soul-admin` ,`soul-bootstrap` 以及你自己的接入项目。


## springMvc & springcloud

* 说白了，你之前怎么请求就怎么请求，没有很大的变动，变动的地方有2点。

* 第一点，你之前请求的域名是你自己的服务，现在要换成网关的域名 （这个你听的懂？）

* 第二点，soul网关需要有一个路由前缀，这个路由前缀就是你接入项目进行配置 `contextPath` ,如果熟的话，可以自由在 `soul-admin` 中的divide插件进行自由更改.
 
```
# 比如你有一个 order服务 它有一个接口，请求路径 http://localhost:8080/test/save

# 现在就需要换成：http://localhost:9195/order/test/save

# 其中 localhost:9195 为网关的ip端口，默认端口是9195 ，/order 是你接入网关配置的 contextPath

# 其他参数，请求方式不变。

# 我讲到这里还不懂？ 请加群问吧

```
* 然后你就可以进行访问了，如此的方便与简单。