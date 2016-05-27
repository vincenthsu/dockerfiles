FROM ubuntu:14.04

MAINTAINER vincenthsu@gorilla-technology.com

WORKDIR /home

RUN \
  apt-get update && \
  apt-get install -y build-essential libc6-dev pkg-config \
        gnupg libsqlite3-dev libcurl4-gnutls-dev libjpeg-dev libpng-dev \
        libopencv-dev libboost-all-dev libssl-dev libcrypto++-dev libsdl2-dev \
        libavcodec-dev libswscale-dev libgstreamer1.0-dev gstreamer1.0-libav \
        libgstreamer0.10-dev libgstreamer-plugins-base0.10-dev \
        libgstreamer-plugins-base1.0-dev && \
  apt-get install -y lighttpd sqlite3 && \
  apt-get install -y wget vim git ssh subversion && \
  apt-get clean && \
  rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

EXPOSE 22:2222
EXPOSE 80:8080
EXPOSE 8000:8000
EXPOSE 53333:53333
