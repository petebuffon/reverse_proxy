FROM nginx

COPY ./conf.d /etc/nginx/conf.d \
  && COPY ./*.pem /etc/nginx/keys/

RUN userdel nginx \
    && useradd -u 2000 nginx \
    && mkdir -p /var/run/nginx /var/tmp/nginx \
    && chown -R nginx:nginx /usr/share/nginx /var/run/nginx /var/tmp/nginx /etc/nginx/conf.d \
    && mkdir /cache && chown -R nginx:nginx /cache

USER nginx:nginx