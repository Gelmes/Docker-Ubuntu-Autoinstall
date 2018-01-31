# Docker-Ubuntu-Autoinstall
Automatically installs docker using the steps provided at [this hopefully not broken link](https://docs.docker.com/install/linux/docker-ce/ubuntu).
I have only tested on my machine so hopefully there is no issues with it.

# One-Step Automated install
`curl -sSL https://raw.githubusercontent.com/Gelmes/Docker-Ubuntu-Autoinstall/master/autoinstall.sh | bash`

# Manual Install
Fallow the guide [Here](https://docs.docker.com/install/linux/docker-ce/ubuntu) for details

```
sudo apt-get remove docker docker-engine docker.io

sudo apt-get update

sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    software-properties-common

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

sudo apt-key fingerprint 0EBFCD88

sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"

sudo apt-get update

sudo apt-get install docker-ce
````

# Check Installation
Run the fallowing command

`sudo docker run hello-world`

You should see something like the fallowing. If not your best next bet is to fallow the docker guide.

```
Hello from Docker!
o generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://cloud.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/engine/userguide/
e fallowing
```

