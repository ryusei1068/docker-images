FROM ubuntu:20.04

USER root
ENV USER root

RUN apt-get update \
    && apt-get install -y \
    apt-utils \
    curl

RUN curl -fsSL https://deb.nodesource.com/setup_21.x | bash - &&\
    apt-get install -y nodejs
