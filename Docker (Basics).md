===== DOCKER =====
====================================================================================================

HOW TO INSTALL DOCKER

```
sudo apt update
```

```
sudo apt install apt-transport-https ca-certificates curl gnupg-agent software-properties-common
```

```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

```
sudo apt update
```

```
sudo apt install docker-ce docker-ce-cli containerd.io
```

```
sudo systemctl status docker
```

============================================================================================

HOW TO UPDATE DOCKER

```
sudo apt update && sudo apt upgrade
```

============================================================================================

PREVENT DOCKER FROM UPDATING

```
sudo apt-mark hold docker-ce
```

============================================================================================

On Centos, only podman is installed by default so use following command to create alias.
This method is temporary.

```
alias docker=podman
```

To make it permanent, do following

```COMMAND     : vim ~/.bashrc```

```ADD TEXT    : alias docker='podman'```

```COMMAND     : source ~/.bashrc```

Restart instance.

============================================================================================

To check if docker is working fine or not use following command:

```
docker run hello-world
```

OR

```
docker container run hello-world
```

If you get output like this,

```Hello from Docker! This message shows that your installation appears to be working correctly.```

Then it is working just fine.

============================================================================================

Executing Docker Commands as a Non-Root User

```
sudo usermod -aG docker <user>
```

============================================================================================

UNINSTALLING DOCKER

```
docker container stop $(docker container ls -aq)
```

```
docker system prune -a --volumes
```

```
sudo apt purge docker-ce
```

```
sudo apt autoremove
```

============================================================================================
