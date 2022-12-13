---
title: Axios
date: 2022-12-8 11:00:26
lang: zh
duration: 10min
description: Axios 的使用与封装
---

## 什么是 Axios

官网上的介绍是这样的：

> Axios is a `promise-based` HTTP Client for *node.js* and the *browser*. It is isomorphic (= it can run in the browser and nodejs with the same codebase). On the server-side it uses the native node.js http module, while on the client (browser) it uses XMLHttpRequests.

翻译过来就是： 

Axios 是一个基于 Promise 的 HTTP 库，可以用在浏览器和 node.js 中。它可以在浏览器和 node.js 中使用同一套代码。在服务端它使用 node.js 的 http 模块，而在客户端（浏览器）它使用 XMLHttpRequests。

## Axios 的特点

1. 在浏览器中发送 `XMLHttpRequests` 请求
2. 在 node.js 中发送 `http` 请求
3. 支持 Promise API
4. 拦截请求和响应
5. 转换请求和响应数据
6. 自动转换 `JSON` 数据
7. 客户端支持防止 [XSRF](https://en.wikipedia.org/wiki/Cross-site_request_forgery)

## 基本使用

```js
axios.get('url', {
  params: {
    name: 'merlin',
  },
}).then((res) => {
  console.log(res.data)
})

axios.post('url', {
  data: {
    name: 'merlin',
  },
}).then((res) => {
  console.log(res.data)
})
```

## Axios 的配置

```js
axios.defaults.baseURL = 'url' // 设置默认的请求地址
axios.defaults.timeout = 1000 // 设置请求超时时间
axios.defaults.headers = {
  'Content-Type': 'application/json',
} // 设置请求头
```

## Axios 的拦截器

```js
// 添加请求拦截器
/**
 * @param {Function} fn1 请求成功的回调
 * @param {Function} fn2 请求失败的回调
 */
axios.interceptors.request.use(fn1, fn2) 

// 添加响应拦截器
/**
 * @param {Function} fnl 响应成功的回调
 * @param {Function} fn2 响应失败的回调
 */
axios.interceptors.response.use(fnl, fn2)
```
