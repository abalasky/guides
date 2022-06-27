# Docker Guide


### Quick Start Commands

**Get help on any command:**
```
docker build --help 
```

**Build a docker image from a Dockerfile:**

* **Format:** `docker build --OPTIONS DOCKERFILEPATH`
```
docker build ---tag hello-world . 
```

```
docker build -t my-app:1.0 . 
```


**List local images:**
```
docker images
```

**Remove local images:**
```
docker rmi IMAGENAME
```

**Start a container from an image:**
```
docker run -p LOCALPORT:CONTAINERPORT --name NAME -d IMAGENAME
```
* `-d` for detached mode, `-p` for port forwarding

**List running containers:**
```
docker ps - a
docker ps
```
* `-a` to see stopped containers

**Check logs of a container:**
```
docker logs -f CONTAINERID
```
* `-f` for tailing the log


**Stop a running container:**
```
docker stop CONTAINERID
```

**Run a stopped container:**
```
docker start CONTAINERID
```

**Remove a stopped container:**
```
docker rm CONTAINERID
```

### Extra Commands

**Share an image to the dockerhub:**

* Step 1 - Tag your image
```
docker tag IMAGE username/IMAGE
```
* Step 2 - Push
```
docker push usdername/IMAGE
```

**Pull an image from the dockerhub:**
```
docker pull username/IMAGE:TAG
```

### Docker Compose Quickstart Commands

```
docker compose up -d
```
* `-d` for detached mode

**Specify a filename:**
```
docker compose -f my-compose.yml up
```

**Remove containers and network:**
```
docker compose -f my-compose.yml down
```


