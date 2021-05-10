# 基础镜像
FROM jenkins/jenkins:lts

# 作者
MAINTAINER Rong.Jia 852203465@qq.com

# 切换root用户
USER root

# 安装依赖
RUN apt-get update \
    && apt-get install -y sudo \
    && rm -rf /var/lib/apt/lists/* \
    && apt-get install -y wget \
    && apt-get install -y unzip
RUN echo "jenkins ALL=NOPASSWD: ALL" >> /etc/sudoers

WORKDIR /opt

# 添加依赖
RUN wget https://mirrors.bfsu.edu.cn/apache/maven/maven-3/3.8.1/binaries/apache-maven-3.8.1-bin.tar.gz \
    && wget https://npm.taobao.org/mirrors/node/v14.16.1/node-v14.16.1-linux-x64.tar.gz \
    && wget https://services.gradle.org/distributions/gradle-7.0-bin.zip \
    && tar zxvf apache-maven-3.8.1-bin.tar.gz \
    && tar zxvf node-v14.16.1-linux-x64.tar.gz \
    && unzip gradle-7.0-bin.zip \
    && rm -rf gradle-7.0-bin.zip node-v14.16.1-linux-x64.tar.gz apache-maven-3.8.1-bin.tar.gz

WORKDIR /

# 安装 maven node
RUN ln -s /opt/apache-maven-3.8.1/bin/mvn /usr/bin/mvn \
    && ln -s /opt/node-v14.16.1-linux-x64/bin/node /usr/bin/node \
    && ln -s /opt/node-v14.16.1-linux-x64/bin/npm /usr/bin/npm \
    && ln -s /opt/node-v14.16.1-linux-x64/bin/npx /usr/bin/npx \
    && ln -s /opt/gradle-7.0/bin/gradle /usr/bin/gradle

# 切换jenkins用户
USER Jenkins














