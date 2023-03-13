# Docker
https://docs.docker.com/desktop/install/ubuntu/  
Устанавливаем docker desktop  
  
`$ sudo apt-get update`  
`$ sudo apt-get install ./docker-desktop-<version>-<arch>.deb`  
  
# image + веб-сервер nginx  
1. Чтобы создать пользовательский образ, необходимо создать `Dockerfile`:  
`FROM nginx:latest  
COPY ./nginx/html/hello.html /usr/share/nginx/html/hello.html`  
  
2. Следующим этапом необходимо выполнить `build`  
`$ docker build -t webserver .`  
  
# Запуск контейнера  
Запустим `image` в контейнере:  
`$ docker run -it --rm -d -p 8080:80 --name web webserver`  
  
# Добавим html страницу
```
<!doctype html>  
<html lang="en">  
<head>  
  <meta charset="utf-8">  
  <title>Docker Nginx</title>  
</head>  
<body>  
  <h2>Hello SIT from DanilPostvaykin!</h2>  
</body>  
</html>
```
  
# Проверяем работоспособность  
![HWDP](https://user-images.githubusercontent.com/71296166/224723757-b9b486e0-813f-45ba-aefc-3afeca8860f2.png)


