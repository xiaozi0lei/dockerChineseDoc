此翻译系列来自于 [虎妞网](http://www.tigerbull.info)，欢迎转载，转载请注明出处，谢谢！

此为开源翻译项目，github仓库为 [dockerChineseDoc](https://github.com/xiaozi0lei/dockerChineseDoc)

***

#[About Docker](http://www.tigerbull.info/)
**Develop, Ship and Run Any Application, Anywhere**

**Docker** is a platform for developers and sysadmins to develop, ship, and run applications. Docker lets you quickly assemble applications from components and eliminates the friction that can come when shipping code. Docker lets you get your code tested and deployed into production as fast as possible.

**开发，运输和运行应用程序，在任何地方**

**Docker** 是一个为研发人员和系统管理员设计的平台，用来开发，运输和运行应用程序的平台。Docker能够帮助你快速从模块装配出应用程序，消除运输代码时产生的摩擦（这里翻译不好，大体意思就是能够快速的将应用程序运行起来，消除各个环节的问题）。Docker帮助你尽可能快的将产品从测试开发状态投入到生产中。

Docker consists of:

* The Docker Engine - our lightweight and powerful open source container virtualization technology combined with a work flow for building and containerizing your applications.
* [Docker Hub](https://hub.docker.com/) - our SaaS service for sharing and managing your application stacks.

Docker 由以下组成：

* Docker 引擎 - 我们提供轻量同时强大的开源容器虚拟化技术结合完整的工作流来构建和容器化你的应用程序。
* [Docker Hub](https://hub.docker.com/) - 我们的分享和管理应用程序库的SaaS(Software as a Service)业务。


##Why Docker?
*Faster delivery of your applications*

* We want your environment to work better. Docker containers, and the work flow that comes with them, help your developers, sysadmins, QA folks, and release engineers work together to get your code into production and make it useful. We've created a standard container format that lets developers care about their applications inside containers while sysadmins and operators can work on running the container in your deployment. This separation of duties streamlines and simplifies the management and deployment of code.
* We make it easy to build new containers, enable rapid iteration of your applications, and increase the visibility of changes. This helps everyone in your organization understand how an application works and how it is built.
* Docker containers are lightweight and fast! Containers have sub-second launch times, reducing the cycle time of development, testing, and deployment.

*快速交付你的应用程序*

* 我们希望你的工作环境更好。Docker 容器及其工作流就是为了帮助你的开发人员，系统管理员，QA和构建工程师一起工作，帮助代码尽早成为产品，发挥它的作用。我们已经创建了一个标准容器格式，让开发人员只关心他们容器里的应用程序，同时在整个开发过程中系统管理员和操作员能够轻松的运行和部署这个容器。这将帮助职责分离，简化管理和代码的部署。
* 我们使之容易构建新的容器，快速迭代你的应用程序，使你更清楚的看到不断的变化。这将帮助你的组织中的每一个人理解你的应用程序如何工作，如何被构建。
* Docker 容器是轻量的和快速的！容器拥有次秒级的运行次数，减少了开发，测试和部署的周期时间。


*Deploy and scale more easily*

* Docker containers run (almost) everywhere. You can deploy containers on desktops, physical servers, virtual machines, into data centers, and up to public and private clouds.
* Since Docker runs on so many platforms, it's easy to move your applications around. You can easily move an application from a testing environment into the cloud and back whenever you need.
* Docker's lightweight containers also make scaling up and down fast and easy. You can quickly launch more containers when needed and then shut them down easily when they're no longer needed.

*更容易的部署和扩展*

* Docker 容器几乎运行在任何地方。你可以将容器部署到台式机，物理服务器，虚拟机，数据中心，甚至共有或者私有的云上。
* 因为Docker容器能够运行在这么多平台上，你可以容易的到处移动你的应用程序。你可以很容易的从一个测试环境移动到云上，也可以随时收回。
* Docker的轻量级容器也能够快速和容易的扩展和缩小。你可以在需要的时候快速的启动更多的容器，在不需要的时候很容易的关闭他们。

*Get higher density and run more workloads*

* Docker containers don't need a hypervisor, so you can pack more of them onto your hosts. This means you get more value out of every server and can potentially reduce what you spend on equipment and licenses.

*获得更高的密度，运行更多工作*

* Docker 容器没有管理程序，因此你可以在你的主机上运行更多的容器。这意味着你将从每一台服务器获得更多的价值，潜在的减少设备和licenses的花销。

*Faster deployment makes for easier management*

* As Docker speeds up your work flow, it gets easier to make lots of small changes instead of huge, big bang updates. Smaller changes mean reduced risk and more uptime.

*快速部署有助于简单管理*

* 由于Docker可以加快你的工作流，因此它适合于管理大量小的改变，而不是巨大的爆炸式的更新。小的改变意味着减少风险和提供更多的运行时间。

##About this guide
The [Understanding Docker section](http://docs.docker.com/introduction/understanding-docker/) will help you:

* See how Docker works at a high level
* Understand the architecture of Docker
* Discover Docker's features;
* See how Docker compares to virtual machines
* See some common use cases.

[理解 Docker 章节]()将帮助你学习：

* 在高level层面，Docker是如何工作的
* 理解Docker的架构
* 了解Docker的特性
* 看到Docker和虚拟机的不同
* 学习一些常用的例子

###Installation Guides
The [installation section](http://docs.docker.com/installation/#installation) will show you how to install Docker on a variety of platforms.

[安装章节]()将向你展示在各种不同的平台如何安装Docker

###Docker User Guide
To learn about Docker in more detail and to answer questions about usage and implementation, check out the [Docker User Guide](http://docs.docker.com/userguide/).

想要学习Docker更多的细节，找到关于使用和实现的问题的答案，请查看[Docker 用户手册]()

###Release Notes
A summary of the changes in each release in the current series can now be found on the separate [Release Notes page](http://docs.docker.com/release-notes/)

[发行说明]()是Docker当前系列的每一个发行版本的变化的总结

###Licensing
Docker is licensed under the Apache License, Version 2.0. See [LICENSE](https://github.com/docker/docker/blob/master/LICENSE) for the full license text.

Docker遵从the Apache License, Version 2.0版权，请查看[版权说明](https://github.com/docker/docker/blob/master/LICENSE)了解细节。