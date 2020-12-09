# version
ARG NODE_VER=15.3.0-buster-slim
ARG ANGULAR_VER=11.0.3

# image
FROM node:${NODE_VER}

RUN apt-get update && apt-get install -y \
  locales-all \
  emacs \
  git \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/*

# 日本語化
ENV LANG ja_JP.UTF-8
ENV LANGUAGE ja_JP:ja
ENV LC_ALL ja_JP.UTF-8

# dotfiles
COPY dotfiles/.emacs.d/init.el /root/.emacs.d/init.el

# angular
RUN npm install -g @angular/cli@${ANGULAR_VER}

EXPOSE 4200
