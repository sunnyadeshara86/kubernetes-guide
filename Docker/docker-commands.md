# Docker Commands

## Installing Docker on Ubuntu VM

> sudo apt-get install docker.io

If you want to use Docker without having to sudo commands, run the following commands:

> sudo groupadd docker
> 
> sudo usermod -aG docker <YOUR_USERNAME>

## Checking if docker is installed and running

> docker --version

## Getting started with Docker images

### Running container using hello-world image

> docker run hello-world

This command will pull the hello-world image from the Docker Hub public repository and run the application in it. If you can run it successfully, you will see this output:

![Docker Run](https://github.com/sunnyadeshara86/kubernetes-guide/blob/master/Docker/Images/docker-run-hello-world.JPG)

### searching for the available NGINX images in Docker Hub

> docker search nginx

The output will show several available images. Usually, the first in the list is the official image.

### Pulling latest NGINX image

> docker pull nginx:latest

This will download the current latest version of the image. The latest keyword after the colon stands for the “tag” of this image. To install a specific version (recommended), specify the tag like this:

> docker pull nginx:1.25.2-alpine-slim

### Running the container using NGINX iamge

> docker run --name nginxcontainer -p 80:80 nginx:1.25.2-alpine-slim

You can use your favourite browser to open the URL using http://<serverip>

### Stopping and Removing nginxcontainer container

> docker stop nginxcontainer
>
> docker rm nginxcontainer

### Listing all the running and stopped containers

> docker ps –a

### Listing all the locally available images

> docker images





