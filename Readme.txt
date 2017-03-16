###############################################
Basic commands used in Docker with Ubuntu OS.
###############################################

In Ubuntu either you have to use ‘sudo’ before each command you run in Ubuntu or you can switch to root user by using ‘sudo -s’ (it will ask for the primary user’s password, when you add this you will be using the terminal as a root user).

#installing Docker in Ubuntu
#updating the repo
apt-get update 

#Add the GPG key for the official Docker repository to the system
apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 58118E89F3A912897C070ADBF76221572C52609D

#Add the Docker repository to APT
apt-add-repository 'deb https://apt.dockerproject.org/repo ubuntu-xenial main'

#Update the package database with the Docker packages
apt-get update

#Install docker
apt-get install -y docker-engine

#check the docker status-it should be on active mode
systemctl status docker

#add a Ubuntu image
docker pull ubuntu:16.04

#check for Docker Containers
docker images

#If we are accessing the container
docker run -it <container ID> /bin/bash

#Check Docker images
Docker ps -a

#Commit the Docker image to a container
docker commit <container_id> cyrilsebastian:ubunodeV1


#Open another terminal and type in the command
docker exec -it <(Image ID)dbbf346b6917> bash

################################################
Building a Docker file.

You need to assemble your DockerFile and the dependent files(hello.js) in one directory

#To build a Docker image run DockerFile from the current directory
docker build -t cyrilsebastian/buildv1 .
