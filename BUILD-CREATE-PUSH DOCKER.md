===== DOCKER LOGIN VIA CLI =====

Enter your username and password
```
docker login
```

===== CREATE DOCKER FILE AND BUILD =====

Create a file directory using mkdir.

Go to the directory

Using vim/nano/gedit create a file named 'Dockerfile' and put your docker content in it and save it.

Now build it using following command,
```
docker build -t <imagename>:<version> .
```
===== CREATE DOCKER IMAGE =====

Now after successful execution, go for next
```
docker images
```

```
docker tag <repo_name>:tag username/repository:tag
```

===== PUSH DOCKER IMAGE =====

If you don't give tag specifically, it will take default tag as 'latest'.
```
docker push username/repository:tag
```

===== REMOVE ALL CONTAINERS, NETWORKS, IMAGES (UNUSED) =====

```
docker system prune -a
```
===== REMOVE IMAGES FORCEFULLY =====

```
docker rmi -f <tag>
```
