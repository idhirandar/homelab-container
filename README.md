# Docker Compose files and some instruction

This reposetory is the collection of comman application which i used in my homelab, I created this repo to help my colleagues.


## Setup base machine for further follow this instruction

In my homelab enviroment [Rocky Linux](https://rockylinux.org/about/#:~:text=It's%20name%20was%20chosen%20as,March%20and%20May%20of%202021.) is the go to linux distro there are plenty of other good distros available you can choose according to your expertise.

## Docker installation

Follow This instruction according to your linux distro

#### On Rockylinux [script](https://gist.github.com/ryanmaclean/91b270d858939729443f889760b4d72f)

```shell
sudo dnf update && sudo apt upgrade -y 
sudo dnf config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
sudo dnf -y install docker-ce docker-ce-cli containerd.io docker-compose-plugin
sudo systemctl --now enable docker
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

## Easy Portainer installed with one command line string 
This is the simplest way to manage docker just paste this line after distro selection.
```bash
docker run -d -p 8000:8000 -p 9443:9443 --name portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v /home/rocky/all-container-data/portainer:/data portainer/portainer-ce:latest
```

![alt text](https://github.com/idhirandar/homelab-container/raw/main/app-screenshot/portainer.png)


## List of all software 


|Se. No| **Name** |  **Discriptions** | **Compose File** | **Offecial Doc**
| :---: | --- | --- | :---: | :---: |
1| portainer | container mgmt UI | [Compose file](https://github.com/idhirandar/homelab-container/blob/main/compose-files/portainer.yml) | [Github](https://github.com/portainer/portainer) |
2| homer dashboard | static dashboard | [Compose file](https://github.com/idhirandar/homelab-container/blob/main/compose-files/homer-dashboard.yml) | [Github](https://github.com/bastienwirtz/homer) |
3| MariaDB | database server | [Compose file](https://github.com/idhirandar/homelab-container/blob/main/compose-files/mariadb.yml) | [Github](https://github.com/MariaDB/mariadb-docker) |
4| PhpMyAdmin | web gui for database server managment | [Compose file](https://github.com/idhirandar/homelab-container/blob/main/compose-files/phpMyAdmin.yml) | [Github](https://github.com/phpmyadmin/docker) |
5| pihole | DNS sinkhole (ad-blocker) | [Compose file](https://github.com/idhirandar/homelab-container/blob/main/compose-files/pihole.yml) | [Github](https://github.com/pi-hole/pi-hole) |
6| lychee | photo gallery server | [Compose file](https://github.com/idhirandar/homelab-container/blob/main/compose-files/lychee.yml) | [github](https://github.com/LycheeOrg/Lychee) |
