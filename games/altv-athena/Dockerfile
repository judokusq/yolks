# ----------------------------------
# Pterodactyl Core Dockerfile
# Environment: Java
# Minimum Panel Version: 0.6.0
# ----------------------------------
FROM alpine:latest

MAINTAINER <robin@kemmler.ruhr>

RUN apk add --no-cache --update curl ca-certificates openssl git tar bash sqlite fontconfig git curl wget nodejs npm libatomic \
    && adduser --disabled-password --home /home/container container

USER container
ENV  USER=container HOME=/home/container

WORKDIR /home/container

COPY ./entrypoint.sh /entrypoint.sh

CMD ["/bin/bash", "/entrypoint.sh"]
