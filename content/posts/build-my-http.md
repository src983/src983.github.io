+++
date = '2026-02-22T17:36:05+08:00'
draft = false
title = 'Build My HTTP'
+++

### Introduction
{{< collapse title="Introduction" open="true" >}}
HTTP（HyperText Transfer Protocol）是构建现代 Web 的核心应用层协议，它定义了客户端（如浏览器）与服务器之间如何进行“对话”。
这个项目是基于 TCP 原语从 0 手写实现一个 HTTP 服务器，即不依赖任何 Web 框架，不使用现成库，基于 Linux Socket API 手写一个 HTTP Server，希望在完成该项目之后对开发者经常调用的API有更清晰的了解，能深入理解网络协议栈与后端服务器工作原理
这个项目是基于 TCP 原语从 0 手写实现一个 HTTP 服务器，即不依赖任何 Web 框架，不使用现成库，基于 Linux Socket API 手写一个 HTTP Server，希望在完成该项目之后对开发者经常调用的 API 有更清晰的了解，能深入理解网络协议栈与后端服务器工作原理。
{{< /collapse >}}

### Why should I build such a project?
{{< collapse title="Why should I build such a project?" >}}
在教学阶段经常听见的一句话就是不要以利益驱动去写代码，这对整个代码生涯来说过于短视；但我认为我们应该更加辩证地看待这件事。当你对一个初学者说：你要训练底层能力，彻底理解 Web 的底层运行机制，建立从操作系统 → 网络 → 协议 → 应用层 的完整认知链条。

我想很多人在刚接触code时，估计会像一个“瀚海里游荡但是迷路的瞎子”，在这个时候总是会接收到各种信息：今天叫你学这个技术明天叫你学那个框架；初学者认识尚浅，容易见风就是雨，又恰逢AI爆发的时代，前端频繁迭代、框架层出不穷，虽然疲于追逐新技术，但却没有接触到底层的基石，执着于“虚无缥缈的东西”上，更严重的问题是这个学点皮毛，那个学点皮毛，浪费了自身的时间和精力，却无法进行有效的积累

To learn how HTTP works, you'll implement your server from scratch using TCP primitives instead of using C++'s built-in HTTP libraries.
{{< /collapse >}}

### 开发过程的一点建议（也可以说是 pre-requisites for this challenge）
{{< collapse title="开发过程的一点建议（也可以说是 pre-requisites for this challenge）" >}}
而且就算在你的开发过程中会直面无数的“长篇小说式”终端错误日志，你也有强大的 AI 模型进行兜底。我的一点小小经验是：很多时候你并不是第一个遇到这个问题的人，你可以通过搜索引擎寻找解决方案或阅读 official docs，甚至将上述方法一并结合到你的开发 workflow 中。
{{< /collapse >}}

### First Step
{{< collapse title="First Step" >}}
You can ignore the contents of the request. We'll cover parsing requests in later stages.
This challenge uses HTTP/1.1.

Note that each header ends in a CRLF, and the entire header section also ends in a CRLF.
{{< /collapse >}}