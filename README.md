# Docker Tutorial

## Sections

- Docker Desktop
- Docker Engine
- Docker Compose

<details>
  <summary> Docker Overview </summary>

## Docker overview

Docker is an open platform for developing, shipping, and running applications. Docker enables you to separate your applications from your infrastructure so you can deliver software quickly. With Docker, you can manage you infrastructure in the same ways you manage your applications. By taking advantage of Docker's methodologies for shipping, testing and deploying code quickly, you can significantly reduce the delay between writing code and running it production. 

## The Docker platform 

Docker provides the ability to package and run an application in a loosely isolated environment called a container. The isolation and security allows you to run many containers simultaneously on a given host. Containers are lightweight and contain everything needed to run the application, so you do not need to rely on what is currently installed on the host. You can easily share containers while you work, and be sure that everyone you share with gets the same container that works in the same way.

Docker provides tooling and a platform to manage the lifecycle of your containers:

- Develop your application and its supporting components using containers.
- The container becomes the unit for distributing and testing your application.
- When you're ready, deploy your application into your prıduction environment, as a container or an orhestrated service. This works the same whether your production environment is a local data center, a cloud provider, or a hybrid of the two.

## What can I use Docker for?

Fast, consistent delivery of your applications

Docker streamlines the development lifecycle by allowing developers to work in standardized environments using local containers which provide your applications and services. Containers are great for continuous integration and continuous delivery (CI/CD) workflows.

Consider the following example scenario:

- Your developers write code locally and share their work with their colleagues using Docker containers.
- They use Docker to push their applications into a test environment and execute automated and manual tests.
- When developers find bugs, they can fix them in the development environment and redeploy them to the test environment for testing and validation.
- When testing in complete, getting the fix to customer is as simple as pushing the updated image to the production environment.
  
</details>

# Docker architecture

Docker uses a client-server architecture. The Docker client talks to the Docker daemon, which does the heavy lifting of building, running, and distributing you Docker containers. The Docker client and daemon can run on the same system, or you can connect a Docker client to a remote Docker daemon. The Docker client and daemon communicate using a REST API, over UNIX sockets or a network interface. Another Docker client is Docker Compose, that lets you work with applications consisting of a set of containers.

<img src="" />

## The Docker daemon

This Docker daemon listens for Docker API requests and manage Docker objects such as images, containers, networks, and volumes. A daemon can also communicate with other daemons to manage Docker services.

## The Docker client

The Docker client is the primary way that many Docker users interact with Docker. When you use commands such as ```docker run```, the client sends these commands to dockerd, which carries them out. The docker commands uses the Docker API. The Docker client can communicate with more than one daemon.

## Docker Desktop

Docker Desktop is an easy-to-install application for your Mac or Windows (now also Linux) environment that enables you to build and share containerized applications and microservices. Docker Desktop includes the Docker daemon, the Docker client, Docker Compose, Docker Content Trust, Kubernetes, and Credential Helper. 

## Docker registries 

A Docker registry stores Docker images. Docker Hub is a public registry that anyone can use, and Docker is configured to look for images on Docker Hub by default. You can even run your own private registry.

When you use the ```docker pull``` or ```docker run``` commands, the required images are pulled from your configured registry. When you use the ```docker push``` command, you image is pushed to your configured registry.

## Docker objects

When you use Docker, you are creating and using images, containers, networks, volumes, plugins, and other objects. This section is a brief overview of some of those objects.

## Images

An image is a read-only template with instructions for creating a Docker container. Often, an image is based on another image, with some additional customization. For example, you may build an image which is based on the ```ubuntu``` image, but installs the Apache web server and your application, as well as the configuration details needed to make your application run.

You might create your own images or you might only use those created by others and published in a registry. To build your own image, you create a Dockerfile with a simple syntax for defining the steps needed to create the image and run it. Each instruction in a Dockerfile creates a layer in the image. When you change the Dockerfile and rebuilt the image, only those layers which have changed are rebuilt. This is part of what makes images so lightweight, small, and fast, when comparted to other virtyalization technologies.

### Containers

A container is a runnable instance of an image. You can cretae, start, stop, move, or delete a container using the Docker API or CLI. You can connect a container to one or more networks, attach storage to it, or even create a new image based on its current state. 
