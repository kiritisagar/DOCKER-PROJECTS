# Containers and virtual machines

![image](https://github.com/user-attachments/assets/8017c445-be73-4b8b-8d09-56afa7882f4a)

# VM:
Virtual Machines are full operating systems running on a physical host, requiring a hypervisor. They are heavier but offer more flexibility and security.

# CONTAINER
Docker Containers are lightweight, portable, and run on any platform that supports Docker. They share the host OS kernel but can run on top of VMs.

Virtual Machines are slow and take a lot of time to boot.
Containers are fast and boots quickly as it uses host operating system and shares the relevant libraries.
Containers do not waste or block host resources unlike virtual machines.
Containers have isolated libraries and binaries specific to the application they are running.
Containers are handled by Containerisation engine.
Docker is one of the containerisation platforms which can be used to create and run containers.

![image](https://github.com/user-attachments/assets/ad84734b-5da1-4208-b928-35b02d07739e)



# Docker architecture

Docker uses a client-server architecture. 
The Docker client talks to the Docker daemon, which does the heavy lifting of building, running, and distributing your Docker containers. 
Docker client and daemon communicate using a REST API, over UNIX sockets or a network interface.

![image](https://github.com/user-attachments/assets/d9ba85c3-6c31-44f1-ba28-59505d3127fc)

# The Docker client

The Client is nothing but a command line interface that allows users to interact with Docker. 
When you use commands such as docker run, the client sends these commands to docker daemon , which carries them out. The docker client uses the Docker API.It can communicate with more than one daemon.

# The Docker daemon
The Docker daemon listens for Docker API requests and manages Docker objects such as images, containers, networks, and volumes.


# Docker registries
A Docker registry stores Docker images. Docker Hub is a public registry that anyone can use, and Docker looks for images on Docker Hub by default. 
You can even run your own private registry. When you use the docker pull or docker run commands, Docker pulls the required images from your configured registry. 
When you use the docker push command, Docker pushes your image to your configured registry.

![image](https://github.com/user-attachments/assets/b2b1005b-4d9a-4b9f-8546-2fddfb3ad229)
