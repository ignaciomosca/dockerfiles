FROM ubuntu
MAINTAINER Ignacio Mosca

RUN apt-get update && apt-get install -y git vim

ENV CONTAINER_USER ignacio
RUN echo "Hola soy," $CONTAINER_USER
RUN useradd $CONTAINER_USER
RUN echo "ALL            ALL = (ALL) NOPASSWD: ALL" >> /etc/sudoers

WORKDIR /home/$CONTAINER_USER
ENV HOME /home/$CONTAINER_USER
ENV SHELL /bin/bash

RUN git clone https://github.com/ignaciomosca/dotfiles.git

RUN cp $HOME/dotfiles/.vimrc $HOME

