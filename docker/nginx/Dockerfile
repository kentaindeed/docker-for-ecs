FROM nginx:stable-alpine

RUN mkdir -p /var/www/vhosts/example.com/public_html
RUN adduser -S www-data -G www-data -u 82 \
    && echo "www-data ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers \
    && echo 'www-data:www-data' | chpasswd
ADD ./nginx.conf /etc/nginx/
ADD ./default.conf /etc/nginx/conf.d/
COPY ./nginx.conf /etc/nginx/nginx.conf