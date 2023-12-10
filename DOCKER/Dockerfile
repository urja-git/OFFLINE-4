FROM ubuntu

MAINTAINER swapnilmahajan30@gmail.com

RUN apt-get update 

WORKDIR /sample-second

RUN apt-get install -y git

RUN apt-get install -y vim && apt-get install -y nginx

EXPOSE 90

COPY index.html /var/www/html

ADD jdk-11.0.20_linux-x64_bin.tar.gz /sample-second

ENTRYPOINT service nginx start && bash



