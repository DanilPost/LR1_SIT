# Docker
https://docs.docker.com/desktop/install/ubuntu/  
Устанавливаем docker desktop  
  
`$ sudo apt-get update`  
`$ sudo apt-get install ./docker-desktop-<version>-<arch>.deb`  
  
# image + веб-сервер nginx  
1. Чтобы создать пользовательский образ, необходимо создать `Dockerfile`:  
`FROM nginx:latest  
COPY ./nginx/html/hello.html /usr/share/nginx/html/hello.html`  
  
2. Необходимо выполнить `build`  
`$ docker build -t webserver .`  
