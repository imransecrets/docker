# docker trounble shoot

* open docker then open terminal and type `docker version`

C:\Users\Asif sb>docker version

Client:

 Cloud integration: v1.0.35+desktop.11
 
 Version:           25.0.3
 
 API version:       1.44
 
 Go version:        go1.21.6
 
 Git commit:        4debf41
 
 Built:             Tue Feb  6 21:13:02 2024
 
 OS/Arch:           windows/amd64
 
 Context:           default
 


Server: Docker Desktop 4.28.0 (139021)

 Engine:
 
  Version:          25.0.3
  
  API version:      1.44 (minimum version 1.24)
  
  Go version:       go1.21.6
  
  Git commit:       f417435
  
  Built:            Tue Feb  6 21:14:25 2024
  
  OS/Arch:          linux/amd64
  
  Experimental:     false
  
 containerd:
 
  Version:          1.6.28
  
  GitCommit:        ae07eda36dd25f8a1b98dfbf587313b99c0190bb
  
 runc:
 
  Version:          1.1.12
  
  GitCommit:        v1.1.12-0-g51d5e94
  
 docker-init:
 
  Version:          0.19.0
  
  GitCommit:        de40ad0
  
* right hand side tray `right click on docker`
* ![image](https://github.com/imransecrets/docker/assets/8496861/8428c08c-65cf-4008-813a-ed6cf4bafc8e)

* select `switch to Window container `
* you will found an error propmt with below wordings:
  
  `Containers feature is disabled. Enable it using the PowerShell script (in an administrative PowerShell)
   and restart your computer before using Docker Desktop:
   Enable-WindowOptionalFeature -  online -  FeatureName $("Microsoft-Hyper-V",  "Containers") -All`

To enable the Containers feature using PowerShell and then restart your computer, you can follow these steps:

Open PowerShell as an administrator.
Run the following command to enable the Containers feature:

`Enable-WindowsOptionalFeature -Online -FeatureName $("Microsoft-Hyper-V", "Containers") -All`

After running the command, it will prompt you to restart your computer to apply the changes. 
Type 'Y' to confirm and press Enter.
Once your computer restarts, 
you should be able to use Docker Desktop with the Containers feature enabled.
* Please make sure to run this command in an administrative PowerShell session to ensure it has the necessary permissions to make changes to Windows features.

* Now again 

C:\Users\Asif sb>docker version

Client:

 Cloud integration: v1.0.35+desktop.11
 
 Version:           25.0.3
 
 API version:       1.44
 
 Go version:        go1.21.6
 
 Git commit:        4debf41
 
 Built:             Tue Feb  6 21:13:02 2024
 
 OS/Arch:           windows/amd64
 
 Context:           default

Server: Docker Desktop 4.28.0 (139021)

 Engine:
 
  Version:          25.0.3
  
  API version:      1.44 (minimum version 1.24)
  
  Go version:       go1.21.6
  
  Git commit:       f417435
  
  Built:            Tue Feb  6 20:55:49 2024
  
  OS/Arch:          windows/amd64
  
  Experimental:     false

# Docker Commands 


# Docker Commands Cheat Sheet

## Chapter 6: Images

### List images

```sh
docker images
```
Lists all images on the Docker host.

### Pull an image
```sh
docker pull <image_name>
```
Downloads an image from a Docker registry.

### Remove an image
```sh
docker rmi <image_id>
```
Deletes an image by its ID.

### Remove multiple images
```sh
docker rmi <image_id1> <image_id2>
```
Deletes multiple images by their IDs.

### Remove all images
```sh
docker rmi $(docker images -q) -f
```
Deletes all images on the system. Note: This only works in a PowerShell terminal on Windows.

## Chapter 7: Containers

### List running containers
```sh
docker ps
```
Lists all running containers.

### List all containers
```sh
docker ps -a
```
Lists all containers, including stopped ones.

### Start a container
```sh
docker start <container_id>
```
Starts a stopped container by its ID.

### Stop a container
```sh
docker stop <container_id>
```
Stops a running container by its ID.

### Remove a container
```sh
docker rm <container_id>
```
Deletes a stopped container by its ID.

### Remove all containers
```sh
docker rm $(docker ps -a -q)
```
Deletes all containers on the system.

## Chapter 8: Containerizing an App

### Build an image from a Dockerfile
```sh
docker build -t <image_name> .
```
Builds an image from a Dockerfile in the current directory.

### Run a container
```sh
docker run -d -p <host_port>:<container_port> <image_name>
```
Runs a container in detached mode and maps a host port to a container port.

## Chapter 9: Multi-container Apps with Compose

### Start services defined in a docker-compose.yml
```sh
docker-compose up
```
Starts services defined in a `docker-compose.yml` file.

### Stop services defined in a docker-compose.yml
```sh
docker-compose down
```
Stops and removes services defined in a `docker-compose.yml` file.

## Chapter 10: Docker Swarm

### Initialize a Swarm
```sh
docker swarm init
```
Initializes a new Swarm.

### Join a Swarm
```sh
docker swarm join --token <token> <manager_ip>:<port>
```
Adds a node to an existing Swarm using a token and manager IP.

### Deploy a stack
```sh
docker stack deploy -c <compose_file> <stack_name>
```
Deploys a new stack using a Compose file.

## Chapter 11: Docker Networking

### List networks
```sh
docker network ls
```
Lists all networks on the Docker host.

### Create a network
```sh
docker network create <network_name>
```
Creates a new network.

### Remove a network
```sh
docker network rm <network_name>
```
Deletes a network by its name.

## Chapter 13: Volumes and Persistent Data

### List volumes
```sh
docker volume ls
```
Lists all volumes on the Docker host.

### Create a volume
```sh
docker volume create <volume_name>
```
Creates a new volume.

### Remove a volume
```sh
docker volume rm <volume_name>
```
Deletes a volume by its name.
```

This `README.md` file provides a clear and concise reference to the Docker commands covered in the book "Docker Deep Dive" along with short comments explaining each command.
  
