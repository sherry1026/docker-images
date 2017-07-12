FROM node:6.11-alpine

RUN apk update && apk add --no-cache --virtual .nodedeps gcc g++ python make libc-dev \
    && npm install -g cnpm --registry=https://registry.npm.taobao.org \
	&& npm install -g pm2
