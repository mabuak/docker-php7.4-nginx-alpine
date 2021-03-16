# Docker PHP-FPM 7.4 & Nginx 1.18.0-r13 on Alpine Linux

Build on [Alpine Linux](http://www.alpinelinux.org/).

You can put your code in src folder.

Usage
-----
Start the Docker containers:

Run :

```
docker run -p 80:80 ramadhan/docker-php7.4-nginx-alpine:latest
```

Docker Compose:

```
version: "2"
services: 
  web:
    image: "ramadhan/docker-php7.4-nginx-alpine:latest"
    container_name: web-rama
    ports:
      - "8080:80"
    privileged: true
    volumes:
      - "..:/home/projects/obvest:cached"
      - ".:/etc/nginx/conf.d:cached"
```


