Web application for financial system - security project
=======================================================

# Running:
    cd mongo-docker-compose
    docker-compose up
    ./initiate
    cd ..
    docker-compose up

This will pull all the images from [Docker index](https://index.docker.io/u/jacksoncage/mongo/) and run all the containers.
Also it will connect application with this mongodb cluster, run nginx image above aplication (running localhost:8080, nginx is running
on localhost:80). Nginx is integrated with modsecurity which behave as WAF.

    Browse: localhost:80

### Install Docker

    sudo apt-get install -y apparmor lxc cgroup-lite curl
    wget -qO- https://get.docker.com/ | sh
    sudo usermod -aG docker YourUserNameHere
    sudo service docker restart

### Install Docker-compose (1.4.2+)

    sudo su
    curl -L https://github.com/docker/compose/releases/download/1.4.2/docker-compose-`uname -s`-`uname -m` > /usr/local/bin/docker-compose
    chmod +x /usr/local/bin/docker-compose
    exit

## Built upon
 - [Docker-compose wait to start](http://brunorocha.org/python/dealing-with-linked-containers-dependency-in-docker-compose.html)
 - [Bi directional docker commuication](http://abdelrahmanhosny.com/2015/07/01/3-solutions-to-bi-directional-linking-problem-in-docker-compose/)
 - [MongoDB Sharded Cluster by Sebastian Voss](https://github.com/sebastianvoss/docker)
 - [MongoDB](http://www.mongodb.org/)
 - [Mongo Docker ](https://github.com/jacksoncage/mongo-docker)
 - [DnsDock](https://github.com/tonistiigi/dnsdock)
 - [Docker](https://github.com/dotcloud/docker/)
 - A boilerplate for **Node.js** web applications.
