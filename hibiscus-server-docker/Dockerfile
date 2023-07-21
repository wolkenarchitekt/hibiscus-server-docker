FROM ubuntu:22.04

ARG HIBISCUS_VERSION=2.10.9

RUN apt-get update \
    && apt-get -y install --no-install-recommends default-jre wget unzip \
    && rm -rf /var/lib/apt/lists/*

RUN wget http://www.willuhn.de/products/hibiscus-server/releases/hibiscus-server-$HIBISCUS_VERSION.zip \
    && unzip hibiscus-server-$HIBISCUS_VERSION.zip -d / \
    && rm hibiscus-server-$HIBISCUS_VERSION.zip

COPY cfg/* /hibiscus-server/cfg

EXPOSE 8080
