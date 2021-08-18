# Disallow robots txt with nginx

- This project is a fork from [repo](https://github.com/pmckeetx/docker-nginx.git)

## Pre-requisites
- Docker
- Docker Compose
- curl

## Running the test
`docker-compose up --build` after this nginx should start at port 80

`curl -is http://localhost/robots.txt -H "Host: disallow.robots.com"` should return a response like
```
HTTP/1.1 200 OK
Server: nginx/1.21.1
Date: Wed, 18 Aug 2021 16:26:29 GMT
Content-Type: text/plain
Content-Length: 26
Connection: keep-alive
Content-Type: text/plain

User-agent: *
Disallow: /

```
