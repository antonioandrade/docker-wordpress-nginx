# WordPress

This Dockerfile installs the latest WordPress version, nginx, php-apc, php-fpm and mysql.

It is fork of [eugeneware/docker-wordpress-nginx](http://github.com/eugeneware/docker-wordpress-nginx), reducing the number of layers and using a different base image. Many thanks to the original author!

## Installation

The quickest way to get this docker image installed is to pull the latest version from the Docker registry:

```bash
docker run -p 8080:80 antonioandrade/wordpress
```

If you'd like to build the image yourself then:

```bash
git clone https://github.com/antonioandrade/docker-wordpress-nginx.git
cd docker-wordpress-nginx
docker build -t="antonioandrade/wordpress" .
```

## Usage

To start a new container using this image run:

```bash
docker run -p 8080:80 antonioandrade/wordpress
```

After starting the container, check to see if it started and the port mapping is correct.  This will also report the port mapping between the docker container and the host machine.

```
docker ps
0.0.0.0:8080 -> 80/tcp wordpress
```

You can the visit the following URL in a browser on your host machine to get started:

[http://127.0.0.1:8080](http://127.0.0.1:8080)