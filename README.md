# Docker+PHP8.2+nginx+SQLite
### Поднимаем контейнеры
```shell
docker-compose up -d
```
### Создаем рабочую папку
```shell
mkdir ./src
```
### Устанавливаем laravel
```shell
docker exec -it laravelapp-php-1 composer create-project laravel/laravel /var/www/application
```
### С миграциями работаем внутри контейнера laravelapp-php-1
```shell
docker exec -it laravelapp-php-1 php /var/www/application/artisan db:seed
```

### Настраиваем xdebug
![xdebug_info.png](docker%2Fphp%2Fxdebug_info.png)