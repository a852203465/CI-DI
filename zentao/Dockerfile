FROM easysoft/zentao:latest

MAINTAINER Rong.Jia Rong.Jia@xdcplus.com

RUN ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
RUN echo 'Asia/Shanghai' >/etc/timezone

RUN  apt-get update \
     && apt-get install -y gcc automake autoconf libtool make \
     && apt-get install -y git subversion