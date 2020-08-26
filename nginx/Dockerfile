FROM nginx

COPY ./nginx.conf /etc/nginx/nginx.conf
COPY ./conf.d /etc/nginx/conf.d
COPY ./keys /etc/nginx/keys

RUN userdel nginx \
    && mkdir /tmp/nginx \
    && useradd -u 2000 nginx \
    && chown -R nginx:nginx /etc/nginx /var/cache/nginx /tmp/nginx

EXPOSE 8080

STOPSIGNAL SIGTERM

USER nginx:nginx

CMD ["nginx", "-g", "daemon off;"]
