FROM ubuntu:20.04
MAINTAINER vincent@tomofun.com
WORKDIR /root
RUN apt-get update \
  && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends \
    build-essential cmake automake libtool m4 bc gawk flex bison pkg-config \
    python squashfs-tools libncurses-dev mtd-utils genext2fs libxml2-dev \
    tzdata git vim tmux bzip2 p7zip zip tree curl \
    bash-completion openssh-client ca-certificates \
    net-tools htop iftop nmap netcat \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN TZ=Asia/Taipei \
  && ln -snf /usr/share/zoneinfo/$TZ /etc/localtime \
  && echo $TZ > /etc/timezone \
  && dpkg-reconfigure -f noninteractive tzdata
RUN mkdir -p /opt/augentix-linux/x86_64-arm \
  && ln -s /root/devel/sdks/augentix/arm-augentix-linux-gnueabi /opt/augentix-linux/x86_64-arm/arm-augentix-linux-gnueabi \
  && ln -s /root/devel/sdks/ambarella/arm-elf-4.5.2 /usr/local/arm-elf \
  && ln -s /root/devel/sdks/ambarella/linaro-armv7ahf-2015.11-gcc5.2 /usr/local/linaro-armv7ahf-2015.11-gcc5.2 \
  && ln -s /root/devel/sdks/ambarella/linaro-multilib-2014.06-gcc4.9 /opt/linaro-multilib-2014.06-gcc4.9
