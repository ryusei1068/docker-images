FROM ubuntu:20.04

USER root
ENV USER root

RUN apt-get update \
    && apt-get install -y \
    apt-utils \
    curl

RUN curl -sL https://deb.nodesource.com/setup_20.x -o /tmp/nodesource_setup.sh \
    && chmod +x /tmp/nodesource_setup.sh \
    && bash /tmp/nodesource_setup.sh -y \
    && rm -rf /tmp/nodesource_setup.sh \
    && apt install nodejs
