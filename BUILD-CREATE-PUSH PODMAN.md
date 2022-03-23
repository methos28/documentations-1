===== PODMAN LOGIN VIA CLI =====

Enter your username and password
```
podman login quay.io
```

===== CREATE PODMAN FILE AND BUILD =====

Create a file directory using mkdir.

Go to the directory

Using vim/nano/gedit create a file named 'Dockerfile' and put your podman content in it and save it.

Now build it using following command,
```
podman build -t <imagename>:<version> .
```
===== CREATE PODMAN IMAGE =====

Now after successful execution, go for next
```
podman images
```

===== PUSH PODMAN IMAGE =====

If you don't give tag specifically, it will take default tag as 'latest'.
```
podman push <repo_name without localhost> quay.io/username/repository:<version>
```

===== REMOVE ALL CONTAINERS, NETWORKS, IMAGES (UNUSED) =====
```
podman system prune -a
```

===== REMOVE IMAGES FORCEFULLY =====

```
podman rmi -f <tag>
```
