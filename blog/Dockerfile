# Base image
FROM dockerfile/nodejs

# Install Ghost
RUN \
  cd /tmp && \
  wget https://ghost.org/zip/ghost-latest.zip && \
  unzip ghost-latest.zip -d /ghost && \
  rm -f ghost-latest.zip && \
  cd /ghost && \
  npm install --production && \
  sed 's/127.0.0.1/0.0.0.0/' /ghost/config.example.js > /ghost/config.js && \
  useradd ghost --home /ghost

# Install Gulp
RUN npm install -g gulp

# Build my Ghost blog theme
RUN \
  curl -L http://github.com/emingchn/my-ghost-theme/tarball/master | tar -xvz && \
  mv emingchn-my-ghost-theme-* source
