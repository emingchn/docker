# Base image
FROM ghost

MAINTAINER Yiming Cheng <emingchn@gmail.com>

# Install Gulp and Bower
RUN npm install -g gulp && npm install -g bower

# Build my Ghost blog theme
RUN \
  curl -L http://github.com/emingchn/my-ghost-theme/tarball/master | tar -xvz && \
  mv emingchn-my-ghost-theme-* source
