FROM nginx

COPY ./nginx.conf /etc/nginx/nginx.conf
COPY ./conf.d /etc/nginx/conf.d
COPY ./keys /etc/nginx/keys

RUN userdel nginx \
    && useradd -u 2000 nginx \
    && chown -R nginx:nginx /etc/nginx /var/cache/nginx

USER nginx:nginx
