FROM node:6-alpine
MAINTAINER R. Stanley Hum <r.stanley.hum@gmail.com>

ENV HUGO_VERSION 0.26
ENV HUGO_BINARY hugo_${HUGO_VERSION}_linux-64bit

RUN apk update && apk --no-cache add ca-certificates wget && update-ca-certificates \
	&& mkdir /usr/local/hugo && cd /usr/local/hugo \
	&& wget https://github.com/spf13/hugo/releases/download/v${HUGO_VERSION}/${HUGO_BINARY}.tar.gz \
	&& tar xzf /usr/local/hugo/${HUGO_BINARY}.tar.gz -C /usr/local/hugo/ \
	&& ln -s /usr/local/hugo/hugo /usr/local/bin/hugo \
	&& rm /usr/local/hugo/${HUGO_BINARY}.tar.gz \
	&& npm install -g firebase-tools

#CMD [ "bin/sh" ]
