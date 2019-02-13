FROM debian:jessie

LABEL maintainer="Chris Fidao"

RUN apt-get update \
    && apt-get install -y nginx \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* \
    && echo "daemon off;" >> /etc/nginx/nginx.conf

ADD default /etc/nginx/sites-available/default
ADD index.html /var/www/html/index.html

EXPOSE 80
CMD ["nginx"]