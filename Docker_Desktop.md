# Docker Desktop

<details>
  <summary> Overview </summary>

## Overview

Docker Desktop is an easy-to-install application for you OS environment that enables you to build and share containerized applications and microservices. Docker Desktop include:
- Docker Engine
- Docker CLU Client
- Docker Compose
- Docker Content Trust
- Kubernetes
- Credential Helper

Docker Desktop works with you choice of development tools and languages and gives you access to a vast library of certified images and templates in Docker Hub (a hub that include many service software). This enables development teams to extend their environment to rapidly auto-build, continously integrate, and collaborate using a secure repository.

Some of the key features of Docker Desktop include:
- Ability to containerize and share any application on any cloud platform, im multiple languages and frameworks
- Easy installation and setup of a complete Docker development environment
- Includes the latest version of Kubernetes
- Automatic updates to keep you up to date and secure
- On Windows, the ability to toggle between Linux and Windows Server environments to build applications
- Fast and reliable performance with native Windows Hyper-V virtualization
- Ability to work natively on Linux through WSL 2 on Windows machines
- Volume mounting for code and data, including file change notifications and easy access to running containers on the localhost network
- In-container development and debugging with supported IDEs
  
</details>

<details>
  <summary> Configure Docker Desktop (Linux) </summary>

## Configure Docker Desktop (Linux)

The Docker Seettings manu allows you to configure your Docker settings such as installation, updates, version channels, Docker Hub login, and more.

On the General tab, you can configure when to start Docker and specify other settings:
- **Start Docker Desktop when you log in**: Automatically starts Docker Desktop when you open your session.
- **Send usage statistics**: Docker Desktop sends diagnostrics, crash reports, and usage data. This information helps Docker improve and troubleshoot the application. Clear the check box to opt out.
- **Show weekly tips**: Displays useful advice and suggestions about using Docker.
- **Open Docker Desktop dashboard at startup**: Auromatically opens the dashboard when starting Docker Desktop.
- **Enable Docker Compose V1/V2 compatibility mode**: Select this option to enable the ```docker-compose``` command to use Docker Compose V2.

## Advanced

Advanced settings are:

- **CPUs**: By default, Docker Desktop is set to use half the number of processors available on the host machine. To increase processing power, set this to a higher number; to decrease, lower the number.
- **Memory**: By default, Docker Desktop is set to use 25% of your host's memory. To increase the RAM, set this to a higher number. To decrease it, lower the number.
- **Swap**: Configure swap file size as needed. The default is 1GB.
- **Disk image location**: Specify the location of the Linux volume where containers and images are stored.

You can also move the disk image to a different location. If you attempt to move a disk image to a location that already has one, you get a prompt asking if you want to use the existing image or replace it.

## File sharing

Use File sharing to allow local directories on the Linux host to be shared with Linux containers. Thisis especially useful for editing source code in an IDE on the host while running and testing the code in a container. By default the ```/home/<user>``` directory is shared. If your project is outside this directory then it must be added to the list. Otherwise you may get ```Mounts denied``` or ```cannot start service``` errors at runtime.

## Docker Engine

The Docker Engine page allows you to configure the Docker deamon to determine how your containers run.

Type a JSON configuration file in the box to configure the daemon settings. For a full list of options, see the Docker Engine dockerd commandline reference. 
  
</details>
