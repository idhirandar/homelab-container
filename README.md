# Docker Compose files and some instruction

This reposetory is the collection of comman application which i used in my homelab, I created this repo to help my colleagues.


## Setup base machine for further follow this instruction

In my homelab enviroment [Rocky Linux](https://rockylinux.org/about/#:~:text=It's%20name%20was%20chosen%20as,March%20and%20May%20of%202021.) is the go to linux distro there are plenty of other good distros available you can choose according to your expertise.

## Docker installation

Follow This instruction according to your linux distro

#### On Rockylinux [script](https://gist.github.com/ryanmaclean/91b270d858939729443f889760b4d72f)

```console
$ sudo dnf update && sudo apt upgrade -y 
$ sudo dnf config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
$ sudo dnf -y install docker-ce docker-ce-cli containerd.io docker-compose-plugin
$ sudo systemctl --now enable docker
```

#### For other distros follow below links

- On Debian [script](https://gist.github.com/angristan/389ad925b61c663153e6f582f7ef370e)
- On Ubuntu [script](https://github.com/docker/docker-install)

# Docker containers management with cli or GUi

To manage docker container application we have multiple ways :-

- Cli base [docker-cli](https://docs.docker.com/engine/reference/commandline/cli/)
```
if you know how to use docker-cli and manage everything with docker-cli you should't be on this repo
```

- Web UI   [portainer](https://docs.portainer.io/)
```
portainer is a lightweight web UI which allows to manage docker application
```

![alt text](https://github.com/idhirandar/homelab-container/raw/main/app-screenshot/portainer.png)


## List of all software 


|Se. No| **Name** |  **Discriptions** | **Link** |
| :---: |---|---|---|
1| portainer | container mgmt UI | [Github](https://github.com/portainer/portainer) |
2| homer dashboard | static dashboard | [Github](https://github.com/bastienwirtz/homer) |
3| MariaDB | database server | [Github](https://github.com/MariaDB/mariadb-docker) |