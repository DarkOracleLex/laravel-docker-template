FROM php:8.1-fpm-alpine

WORKDIR /var/www

RUN apk update && apk add \
    shadow

# Создаём пользователя и группу www для приложения Laravel
RUN groupadd -g 1000 www
RUN useradd -u 1000 -ms /bin/bash -g www www

# Меняем пользователя на www
USER www

# В контейнере открываем 9000 порт
EXPOSE 9000
CMD ["php-fpm"]
