# Docker-0-to-100
This project demonstrates learning Docker from beginner to advanced by installing Docker on an Ubuntu EC2 instance, creating and managing containers, working with images, volumes, and networks, and performing port mapping. It showcases practical containerization skills and understanding of Docker fundamentals in a cloud environment. 🐳
# Docker Commands Practice on AWS EC2 (Ubuntu)

## Overview
This project documents the basic Docker commands practiced on an AWS EC2 Ubuntu instance. The goal was to learn how to install Docker, run containers, manage images, volumes, and networking.

---
# Docker Practice on AWS EC2 (Ubuntu)

## Project Overview

This project demonstrates Docker installation and basic Docker operations performed on an Ubuntu EC2 instance. It includes working with Docker images, containers, volumes, networks, and port mapping.

---

## 1. Install Docker

Update system packages:

```bash
sudo apt update
sudo apt install docker.io -y
```

Check Docker version:

```bash
docker --version
```

Start Docker service:

```bash
sudo systemctl start docker
sudo systemctl enable docker
```

Test Docker:

```bash
sudo docker run hello-world
```

---

## 2. Docker Images

Pull an image:

```bash
sudo docker pull ubuntu
```

List images:

```bash
sudo docker images
```

Remove image:

```bash
sudo docker rmi ubuntu
```

---

## 3. Docker Containers

Run container:

```bash
sudo docker container run -it -d --name mycon ubuntu
```

Run container with port mapping:

```bash
sudo docker container run -it -d -p 85:80 --name webapp ubuntu
```

List running containers:

```bash
sudo docker ps
```

List all containers:

```bash
sudo docker ps -a
```

Stop container:

```bash
sudo docker stop webapp
```

Remove container:

```bash
sudo docker rm webapp
```

---

## 4. Access Container

Enter container terminal:

```bash
sudo docker exec -it webapp bash
```

Exit container:

```bash
exit
```

---

## 5. Docker Volumes

Create volume:

```bash
docker volume create myvolume
```

List volumes:

```bash
docker volume ls
```

Inspect volume:

```bash
docker volume inspect myvolume
```

---

## 6. Docker Networks

List networks:

```bash
docker network ls
```

Create network:

```bash
docker network create mynetwork
```

Inspect network:

```bash
docker network inspect mynetwork
```

---

## 7. Port Mapping Example

```bash
sudo docker container run -it -d -p 85:80 --name webapp ubuntu
```

Access the container service using:

http://EC2-PUBLIC-IP:85

---

## Conclusion

This project helped in understanding Docker basics including installation, container creation, image management, volume usage, networking, and port mapping in a cloud environment.

