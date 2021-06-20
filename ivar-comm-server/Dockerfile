FROM ubuntu:14.04

MAINTAINER vincenthsu@gorilla-technology.com

WORKDIR /home

RUN \
  apt-get update && \
  apt-get install -y libboost-all-dev libssl-dev && \
  apt-get install -y wget vim git ssh subversion && \
  apt-get clean && \
  rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

EXPOSE 22:2222
EXPOSE 80:8080
EXPOSE 8000:8000
EXPOSE 53333:53333
