#This is a copy from: libray/python:3.6-alpine with just a different base image
FROM iocanel/gosu:latest

MAINTAINER Ioannis Canellos <iocanel@gmail.com>

RUN apk update && apk add vim

RUN mkdir -p /usr/local/share
COPY files /usr/local/share/vim

COPY entrypoint.sh /usr/local/bin/copy-vimfiles-and-start.sh

ENTRYPOINT ["adduser-and-run.sh", "copy-vimfiles-and-start.sh"]
