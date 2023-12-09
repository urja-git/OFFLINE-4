FROM ubuntu

MAINTAINER swapnilmahajan30@gmail.com

RUN apt-get update 

RUN apt-get install -y git

RUN apt-get install -y vim && apt-get install -y nginx

COPY index.html /var/www/html

ENTRYPOINT service nginx start && bash



