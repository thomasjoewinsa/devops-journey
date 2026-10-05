# Day 3 - Docker

## Topics Learned

* Docker Commands
* Docker Snapshot
* Dockerfile
* Docker Network

## 1. Docker Commands

Docker provides commands to create, manage, and interact with Docker images and containers.

### Check Docker Version

```bash
docker --version
```

Shows the installed Docker version.

### Download an Image

```bash
docker pull nginx
```

Downloads the Nginx image from Docker Hub.

### List Docker Images

```bash
docker images
```

Shows the Docker images available on the local machine.

### List Running Containers

```bash
docker ps
```

Shows currently running containers.

### List All Containers

```bash
docker ps -a
```

Shows both running and stopped containers.

### Run a Container

```bash
docker run nginx
```

Creates and starts a container using the Nginx image.

### Stop a Container

```bash
docker stop <container-id>
```

Stops a running container.

### Remove a Container

```bash
docker rm <container-id>
```

Removes a stopped container.

### Remove an Image

```bash
docker rmi <image-name>
```

Removes a Docker image from the local machine.

---

## 2. Docker Snapshot

A Docker snapshot can refer to saving the current state of a container as a new Docker image.

The commonly used command is:

```bash
docker commit <container-id> <image-name>
```

### Example

```bash
docker commit mycontainer myimage:1.0
```

This creates a new image from the current state of the container.

The new image can then be viewed using:

```bash
docker images
```

---

## 3. Dockerfile

A Dockerfile is a text file containing instructions used to build a Docker image.

### Example Dockerfile

```dockerfile
FROM nginx

COPY index.html /usr/share/nginx/html/

EXPOSE 80
```

### Explanation

* `FROM` specifies the base image.
* `COPY` copies files from the local machine into the image.
* `EXPOSE` documents the port used by the application.

### Build an Image

```bash
docker build -t myimage .
```

The `-t` option gives the image a name.

The `.` tells Docker to use the current directory as the build context.

### Run the Image

```bash
docker run -d -p 8080:80 --name mycontainer myimage
```

The application can then be accessed through:

```text
http://localhost:8080
```

---

## 4. Docker Network

A Docker network allows Docker containers to communicate with each other.

### List Networks

```bash
docker network ls
```

Displays the available Docker networks.

### Create a Network

```bash
docker network create mynetwork
```

Creates a new Docker network.

### Run a Container on a Network

```bash
docker run -d --name container1 --network mynetwork nginx
```

This starts an Nginx container and connects it to `mynetwork`.

### Inspect a Network

```bash
docker network inspect mynetwork
```

Displays detailed information about the network and the containers connected to it.

### Remove a Network

```bash
docker network rm mynetwork
```

Removes the Docker network.

---

## Key Takeaway

On Day 3, I learned important Docker concepts including commonly used Docker commands, creating Docker snapshots using `docker commit`, creating images using a Dockerfile, and connecting containers using Docker networks.

**Status: Day 3 Completed**
