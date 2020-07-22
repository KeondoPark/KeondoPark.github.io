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
