此翻译系列来自于 [虎妞网](http://www.tigerbull.info)，欢迎转载，转载请注明出处，谢谢！

此为开源翻译项目，github仓库为 [dockerChineseDoc](https://github.com/xiaozi0lei/dockerChineseDoc)

***

#[Understanding Docker](http://www.tigerbull.info/)

**What is Docker?**

Docker is an open platform for developing, shipping, and running applications. Docker is designed to deliver your applications faster. With Docker you can separate your applications from your infrastructure AND treat your infrastructure like a managed application. Docker helps you ship code faster, test faster, deploy faster, and shorten the cycle between writing code and running code.

`Docker 是一个应用程序开发，运输和运行的开放平台。Docker 是为快速交付你的应用程序而设计的。使用Docker，你的应用程序和你的基础设施是分离的，而且你可以把你的基础设施当做应用程序来管理。Docker帮助你快速的运输代码，快速的测试，快速的部署，从而缩短从开发代码到运行代码的周期时间。`

Docker does this by combining a lightweight container virtualization platform with workflows and tooling that help you manage and deploy your applications.

`Docker 通过绑定一个轻量级的容器虚拟化平台和工作流及其工具包，来帮助你管理和部署你的应用程序。`

At its core, Docker provides a way to run almost any application securely isolated in a container. The isolation and security allow you to run many containers simultaneously on your host. The lightweight nature of containers, which run without the extra load of a hypervisor, means you can get more out of your hardware.

`在Docker的核心，Docker提供一种方式运行几乎所有应用程序在一个隔离的安全的容器内。这些优点允许你在主机上同时运行许多容器。这个原生的轻量级的容器，不需要外部的管理程序就可以运行，意味着你可以从你的硬件中获得更多的价值。`

Surrounding the container virtualization are tooling and a platform which can help you in several ways:

* getting your applications (and supporting components) into Docker containers
* distributing and shipping those containers to your teams for further development and testing
* deploying those applications to your production environment, whether it be in a local data center or the Cloud.

`环绕着容器虚拟化的是能帮助你以下方面的工具和平台：`

* `帮助你将应用程序放入到Docker容器中`
* `分发和运输容器到你的团队中进一步开发和测试`
* `不管生产环境是本地的数据中心还是云，都能轻松部署应用程序到你的生产环境`

###What can I use Docker for?

*Faster delivery of your applications*

Docker is perfect for helping you with the development lifecycle. Docker allows your developers to develop on local containers that contain your applications and services. It can then integrate into a continuous integration and deployment workflow.

For example, your developers write code locally and share their development stack via Docker with their colleagues. When they are ready, they push their code and the stack they are developing onto a test environment and execute any required tests. From the testing environment, you can then push the Docker images into production and deploy your code.

*`快速交付你的应用程序`*

`Docker 非常有助于你的开发周期。Docker可以让你的开发团队在本地的容器内运行你的应用和业务。Docker可以整合到持续集成和开发的工作流中`

*Deploying and scaling more easily*

Docker's container-based platform allows for highly portable workloads. Docker containers can run on a developer's local host, on physical or virtual machines in a data center, or in the Cloud.

Docker's portability and lightweight nature also make dynamically managing workloads easy. You can use Docker to quickly scale up or tear down applications and services. Docker's speed means that scaling can be near real time.

*`很容易的部署和扩展应用程序`*

`Docker 是一个为灵活便携设计的容器平台。Docker容器可以运行在开发者本地机器上，数据中心的物理机或者虚拟机上，甚至你可以在云上运行。`
`Docker 的便携性和轻量的原生特点使动态管理负载变的很简单。你可以使用Docker快速的扩展和缩小应用程序和业务。Docker 具有近实时的扩展效果。`

*Achieving higher density and running more workloads*

Docker is lightweight and fast. It provides a viable, cost-effective alternative to hypervisor-based virtual machines. This is especially useful in high density environments: for example, building your own Cloud or Platform-as-a-Service. But it is also useful for small and medium deployments where you want to get more out of the resources you have.

*`实现更高的密度，运行更多的负载`*

`Docker 轻量的，快速的。相对于基于管理程序的虚拟机，docker 提供了一个可行的，高效的备选方案。在高密度环境中这是特别有帮助的：例如，构建你自己的云或者PaaS平台。但是当你需要更多的资源时，Docker 同样适用于小型和中型的部署环境。`

###What are the major Docker components?

Docker has two major components:

* Docker: the open source container virtualization platform.
* [Docker Hub](https://hub.docker.com/): our Software-as-a-Service platform for sharing and managing Docker containers.

> Note: Docker is licensed under the open source Apache 2.0 license.

###What is Docker's architecture?

Docker uses a client-server architecture. The Docker client talks to the Docker daemon, which does the heavy lifting of building, running, and distributing your Docker containers. Both the Docker client and the daemon can run on the same system, or you can connect a Docker client to a remote Docker daemon. The Docker client and daemon communicate via sockets or through a RESTful API.

![Docker Architecture Diagram](https://docs.docker.com/article-img/architecture.svg)

####The Docker daemon

As shown in the diagram above, the Docker daemon runs on a host machine. The user does not directly interact with the daemon, but instead through the Docker client.

####The Docker client

The Docker client, in the form of the `docker` binary, is the primary user interface to Docker. It accepts commands from the user and communicates back and forth with a Docker daemon.

####Inside Docker

To understand Docker's internals, you need to know about three components:

* Docker images.
* Docker registries.
* Docker containers.

####Docker images

A Docker image is a read-only template. For example, an image could contain an Ubuntu operating system with Apache and your web application installed. Images are used to create Docker containers. Docker provides a simple way to build new images or update existing images, or you can download Docker images that other people have already created. Docker images are the **build** component of Docker.

####Docker Registries

Docker registries hold images. These are public or private stores from which you upload or download images. The public Docker registry is called Docker Hub. It provides a huge collection of existing images for your use. These can be images you create yourself or you can use images that others have previously created. Docker registries are the __distribution__ component of Docker.

####Docker containers

Docker containers are similar to a directory. A Docker container holds everything that is needed for an application to run. Each container is created from a Docker image. Docker containers can be run, started, stopped, moved, and deleted. Each container is an isolated and secure application platform. Docker containers are the **run** component of Docker.

###So how does Docker work?

So far, we've learned that:

1. You can build Docker images that hold your applications.
2. You can create Docker containers from those Docker images to run your applications.
3. You can share those Docker images via Docker Hub or your own registry.

Let's look at how these elements combine together to make Docker work.

####How does a Docker Image work?

We've already seen that Docker images are read-only templates from which Docker containers are launched. Each image consists of a series of layers. Docker makes use of [union file systems](http://en.wikipedia.org/wiki/UnionFS) to combine these layers into a single image. Union file systems allow files and directories of separate file systems, known as branches, to be transparently overlaid, forming a single coherent file system.

One of the reasons Docker is so lightweight is because of these layers. When you change a Docker image—for example, update an application to a new version— a new layer gets built. Thus, rather than replacing the whole image or entirely rebuilding, as you may do with a virtual machine, only that layer is added or updated. Now you don't need to distribute a whole new image, just the update, making distributing Docker images faster and simpler.

Every image starts from a base image, for example `ubuntu`, a base Ubuntu image, or `fedora`, a base Fedora image. You can also use images of your own as the basis for a new image, for example if you have a base Apache image you could use this as the base of all your web application images.

> Note: Docker usually gets these base images from Docker Hub.

Docker images are then built from these base images using a simple, descriptive set of steps we call instructions. Each instruction creates a new layer in our image. Instructions include actions like:

* Run a command.
* Add a file or directory.
* Create an environment variable.
* What process to run when launching a container from this image.

These instructions are stored in a file called a `Dockerfile`. Docker reads this `Dockerfile` when you request a build of an image, executes the instructions, and returns a final image.

####How does a Docker registry work?

The Docker registry is the store for your Docker images. Once you build a Docker image you can push it to a public registry Docker Hub or to your own registry running behind your firewall.

Using the Docker client, you can search for already published images and then pull them down to your Docker host to build containers from them.

[Docker Hub](https://hub.docker.com/) provides both public and private storage for images. Public storage is searchable and can be downloaded by anyone. Private storage is excluded from search results and only you and your users can pull images down and use them to build containers. You can [sign up for a storage plan here](https://hub.docker.com/plans).

####How does a container work?

A container consists of an operating system, user-added files, and meta-data. As we've seen, each container is built from an image. That image tells Docker what the container holds, what process to run when the container is launched, and a variety of other configuration data. The Docker image is read-only. When Docker runs a container from an image, it adds a read-write layer on top of the image (using a union file system as we saw earlier) in which your application can then run.

####What happens when you run a container?

Either by using the docker binary or via the API, the Docker client tells the Docker daemon to run a container.

```bash
$ sudo docker run -i -t ubuntu /bin/bash
```

Let's break down this command. The Docker client is launched using the `docker` binary with the `run` option telling it to launch a new container. The bare minimum the Docker client needs to tell the Docker daemon to run the container is:

* What Docker image to build the container from, here `ubuntu`, a base Ubuntu image;
* The command you want to run inside the container when it is launched, here `/bin/bash`, to start the Bash shell inside the new container.

So what happens under the hood when we run this command?

In order, Docker does the following:

* __Pulls the `ubuntu` image:__ Docker checks for the presence of the `ubuntu` image and, if it doesn't exist locally on the host, then Docker downloads it from [Docker Hub](https://hub.docker.com/). If the image already exists, then Docker uses it for the new container.
* __Creates a new container:__ Once Docker has the image, it uses it to create a container.
* __Allocates a filesystem and mounts a read-write layer:__ The container is created in the file system and a read-write layer is added to the image.
* __Allocates a network / bridge interface:__ Creates a network interface that allows the Docker container to talk to the local host.
* __Sets up an IP address:__ Finds and attaches an available IP address from a pool.
* __Executes a process that you specify:__ Runs your application, and;
* __Captures and provides application output:__ Connects and logs standard input, outputs and errors for you to see how your application is running.

You now have a running container! From here you can manage your container, interact with your application and then, when finished, stop and remove your container.

####The underlying technology

Docker is written in Go and makes use of several Linux kernel features to deliver the functionality we've seen.

#####Namespaces

Docker takes advantage of a technology called `namespaces` to provide the isolated workspace we call the container. When you run a container, Docker creates a set of namespaces for that container.

This provides a layer of isolation: each aspect of a container runs in its own namespace and does not have access outside it.

Some of the namespaces that Docker uses are:

* __The `pid` namespace:__ Used for process isolation (PID: Process ID).
* __The `net` namespace:__ Used for managing network interfaces (NET: Networking).
* __The `ipc` namespace:__ Used for managing access to IPC resources (IPC: InterProcess Communication).
* __The `mnt` namespace:__ Used for managing mount-points (MNT: Mount).
* __The `uts` namespace:__ Used for isolating kernel and version identifiers. (UTS: Unix Timesharing System).

#####Control groups

Docker also makes use of another technology called `cgroups` or control groups. A key to running applications in isolation is to have them only use the resources you want. This ensures containers are good multi-tenant citizens on a host. Control groups allow Docker to share available hardware resources to containers and, if required, set up limits and constraints. For example, limiting the memory available to a specific container.

#####Union file systems

Union file systems, or UnionFS, are file systems that operate by creating layers, making them very lightweight and fast. Docker uses union file systems to provide the building blocks for containers. Docker can make use of several union file system variants including: AUFS, btrfs, vfs, and DeviceMapper.

#####Container format

Docker combines these components into a wrapper we call a container format. The default container format is called `libcontainer`. Docker also supports traditional Linux containers using [LXC](https://linuxcontainers.org/). In the future, Docker may support other container formats, for example, by integrating with BSD Jails or Solaris Zones.

####Next steps
#####Installing Docker

Visit the [installation section](https://docs.docker.com/installation/#installation).

#####The Docker User Guide

[Learn Docker in depth](https://docs.docker.com/userguide/).