# How to create Docker image
Open powershell in VScode and run the following command to access the shell to run script
```
docker build -t hello-docker:1.0.0 .
```
- **here `hello-docker` is image Name and `1.0.0` is image version/ Tag**

# How to see Docker image
Open powershell in VScode and run the following command to access the shell to run script

```
docker images
```

# How to remove image
Open powershell in VScode and run the following command to access the shell to run script

```
docker rmi f78
```
- here f78 is image ID
  

# How to Run Docker container from image
Open powershell in VScode and run the following command to access the shell to run script

```
docker run -d --name first-container -p 8080:80 hello-docker:1.0.0
```
- `-d` means `disconnect`. If vsCode is shutdown, the container will still be running.
- here `first-container` is container name
- `8080` is machine port and `80` is container port.
- `hello-docker:1.0.0` is image name and version/tag.
- go to browser and type in address bar `localhost/8080` to see the local website.
- Then you will find webserver running in container

## Show Which Container is Running
Open powershell in VScode and run the following command to access the shell to run script

```
docker ps -a
```
- -a show all container including running and closed

this will give output:
```
REPOSITORY     TAG       IMAGE ID       CREATED       SIZE
hello-docker   1.0.0     29091019a0b2   2 hours ago   55MB
```
- here 290.. is container id

# How to stop container
Open powershell in VScode and run the following command to access the shell to run script

```
docker stop 5c3
```
- here 5c3 is container ID

# How to start container
Open powershell in VScode and run the following command to access the shell to run script

```
docker start 5c3
```
- here 5c3 is container ID

# How to remove container
Open powershell in VScode and run the following command to access the shell to run script

```
docker rm 5c3
```
- here 5c3 is container ID
