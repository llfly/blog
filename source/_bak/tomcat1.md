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



### 连接器






### 容器


https://yq.aliyun.com/articles/20169


http://www.iocoder.cn/Tomcat/yuliu/Start-analysis-1-start-script/
http://www.iocoder.cn/Tomcat/yuliu/Start-analysis-2-Bootstrap/
http://www.iocoder.cn/Tomcat/yuliu/Start-analysis-3-Digester/






https://github.com/tiann/markdown-img-upload


### 加载器
1. 部署在同一个服务器上的两个 Web 应用程序所使用的 Java 类库可以实现相互隔离。
    两个不同的应用程序可能会依赖同一个第三方类库的不同版本，不能要求一个类库在一个服务器中只有一份
2. 部署在同一个服务器上的两个 Web 应用程序所使用的 Java 类库可以互相共享。
    多份 Spring 分别存放在各个应用程序的隔离目录中，虚拟机的方法去很容易出现过度膨胀的风险   
3. 服务器需要尽可能的保证自身的安全不受部署的 Web 应用程序影响
    Tomcat 也由 Java 语言实现的，因此服务器本身也有类库依赖的问题，基于安全考虑，服务器所使用的类库应与应用程序的类库互相独立
4. 支持 JSP 应用的 Web 服务器，大多数都需要支持 HotSwap 功能
    JSP 文件最终要编译成 Java Class 才能由虚拟机执行，但 JSP 文件由于其纯文本存储的特性，运行时修改的概率远大于第三方类库或程序自身的 Class 文件