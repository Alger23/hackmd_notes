# Ubuntu 18.04 安裝 Docker

## 安裝 Docker

在 Ubuntu Linux 中，使用 apt 安裝 Docker：
```
sudo apt-get update
sudo apt-get install docker.io
```

安裝好可以查一下 docker 服務是否有正常啟動：
```
service docker status
或
systemctl status docker
```

查看 安裝的版本資訊：
```
sudo docker version
```

```
Client:
 Version:           19.03.6
 API version:       1.40
 Go version:        go1.12.17
 Git commit:        369ce74a3c
 Built:             Fri Feb 28 23:45:43 2020
 OS/Arch:           linux/amd64
 Experimental:      false

Server:
 Engine:
  Version:          19.03.6
  API version:      1.40 (minimum version 1.12)
  Go version:       go1.12.17
  Git commit:       369ce74a3c
  Built:            Wed Feb 19 01:06:16 2020
  OS/Arch:          linux/amd64
  Experimental:     false
 containerd:
  Version:          1.3.3-0ubuntu1~18.04.2
  GitCommit:        
 runc:
  Version:          spec: 1.0.1-dev
  GitCommit:        
 docker-init:
  Version:          0.18.0
  GitCommit:        
```


## 取得 Docker Container 映像檔

安裝好 Docker 之後，接著要下載 Container 的映像檔。預設會到 Docker Hub 找公開的映像檔。這裡以 ubuntu 的映像檔做練習：

```
sudo docker search ubuntu
```

```
sudo docker search ubuntu-19
NAME                                          DESCRIPTION                                     STARS               OFFICIAL            AUTOMATED
dokken/ubuntu-19.10                           ubuntu-19.10 image for use with kitchen-dokk…   0                                       
diodonfrost/ubuntu-19.04-ansible              Provides docker containers use for testing a…   0                                       
sannysanoff/ubuntu-19.10-zapcc-dev            Ubuntu 19.10 + zapcc                            0                                       
mesaguy/ubuntu-19.04-boot-x86_64              Ubuntu 19.04 image, bootable for testing pur…   0                                       
pjflores/ubuntu-19.04                                                                         0                                       
mesaguy/ubuntu-19.04-kitchen-ansible-x86_64   Ubuntu 19.04 image for testing Ansible playb…   0                                       
diodonfrost/ubuntu-19.04-puppet               Provides dockerfiles with puppet and in some…   0                                       
mesaguy/ubuntu-19.10-boot-x86_64              Ubuntu 19.10 image, bootable for testing pur…   0                                       
mesaguy/ubuntu-19.10-kitchen-ansible-x86_64   Ubuntu 19.10 image for testing Ansible playb…   0                                       
hyp3rsonix/ubuntu-1904-baseimage-amd64                                                        0                                       
wallezz/ubuntu-19.10-shellinabox                                                              0                                       
gjorgjit/ubuntu-1904                                                                          0                                       
mgrechukh/ubuntu-1910-postfix                                                                 0                                       
rosecompiler/ubuntu-19.04                                                                     0                                       
wallezz/ubuntu-19.04-shellinabox                                                              0                                       
solozzan/ubuntu-19.10                         A simple Ubuntu 19.10 image                     0                                       
simonpzh/ubuntu-19.10-mpich                                                                   0                                       
mtola/ubuntu-19.10-mepp2                                                                      0                                       
markchristopherwest/ubuntu-19.04                                                              0      
```


下載 Container 映像檔，預設會下載 tag 為 latest 的映像檔
```
sudo docker pull dokken/ubuntu-19.10
或是
sudo docker pull dokken/ubuntu-19.10:latest
```

