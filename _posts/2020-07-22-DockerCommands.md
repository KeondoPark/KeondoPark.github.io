---
title: "Docker commands"
date: 2020-07-22 
categories: jekyll update
---
Summary of basic docker commands

Create docker from dockerfile script.

This command uses "research/object_detection/dockerfiles/tf2/Dockerfile" as script and create a new image as "od"

```
sudo docker build -f research/object_detection/dockerfiles/tf2/Dockerfile -t od .
```

Start a docker container from image(od) as interactive mode(-it)
```
sudo docker run -it od
```

See all running docker containers
```
sudo docker container ls
```

See all docker containers(Including stopped containers)
```
sudo docker container ls -a
```

See all docker images
```
sudo docker images
```

Remove container
```
sudo docker rm [Container id]
```
Remove image
```
sudo docker rmi [Image id]
```

Get out of container: Interactive mode to Daemon mode
```
Ctrl + p, Ctrl + q
```
Go into container
```
sudo docker exec -it [Container name] bash 
```

Docker commit(Dockerhub account required and repository should be created before)
```
sudo docker login
docker tag od gundo0102/test			#Tag image, it should be same as the name of repository
sudo docker commit -m "Message" -a "Name" gundo0102/test #Repository name same as tag
```

Copy file into a container
```
sudo docker cp [filename] [containerid]:[address]


