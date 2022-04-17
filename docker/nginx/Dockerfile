FROM nginx:1.20-alpine

COPY ./docker/nginx/default.conf /etc/nginx/conf.d/default.conf
COPY ./docker/nginx/nginx.conf /etc/nginx/nginx.conf
COPY ./src /var/www/html
EXPOSE 80