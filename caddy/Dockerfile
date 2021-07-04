FROM caddy:2.4.3

RUN apk update \
    && apk add --upgrade --no-cach sudo \
    && apk add nss-tools

# create worker-caddy user and group
RUN addgroup -S worker-caddy && adduser -S worker-caddy -G worker-caddy
# allow worker-caddy to use sudo with copy command
RUN echo "worker-caddy ALL = NOPASSWD: /usr/bin/caddy" | tee -a /etc/sudoers

USER worker-caddy

CMD ["sudo", "caddy", "run", "--config", "/etc/caddy/Caddyfile", "--adapter", "caddyfile"]