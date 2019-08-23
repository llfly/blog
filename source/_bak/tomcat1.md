---
title: Tomcat Architecture
categories: 
    - java web
    - tomcat
date: {{ date }}
---

### 需求
Tomcat 需要实现 2 个核心功能，为此抽象了两个核心组件
- 处理 Socket 连接，负责网络字节流与 Request 和 Response 对象的转化 -- （Connector(连接器): 负责对外交流）
- 记载和管理 Servlet，以及具体处理 Request 请求 -- (Container(容器)：负责内容处理)


https://github.com/tiann/markdown-img-upload