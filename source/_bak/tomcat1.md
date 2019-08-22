---
title: Tomcat 学习笔记 - servlet
tags: 
    - tomcat
    - servlet
date: {{ date }}
---

### 什么是 servlet?
- servlet 技术
- servlet 接口
- servlet 容器

2. 为什么存在？

3. 解决了什么问题？
- 早期的 Web 应用主要用于浏览静态页面，HTTP 服务器（Apache、Nginx）向浏览器返回静态 HTML，浏览器负责解析 HTML，将结果呈现给用户,随着互联网发展，需要通过交互操作获取动态结果，也就需要一些扩展机制能够让 HTTP 服务器调用服务端程序
- Sun 公司推出了 servlet 技术，可以把 Servlet 简单理解为运行在服务端的 Java 小程序，但 Servlet 没有 main 方法，不能独立运行，因此必须把它部署到 Servlet 容器中，由容器来实例化并调用 Servlet
- Tomcat 和 Jetty 就是一个 Servlet 容器，为了方便使用，它们也具备 HTTP 服务器的功能，因此 Tomcat 或者 Jetty 就是一个 “HTTP 服务器 + Servlet 容器”，我们也叫它们 Web 容器
- 其他应用服务器比如 Jboss 和 WebLogic，它们不仅有 Servlet 容器的功能，也包含 EJB 容器，是完整的 Java EE 应用服务器，从这个角度看，Tomcat 和 Jetty 算是轻量级的应用服务器


4. 和 spring mvc 的区别是？