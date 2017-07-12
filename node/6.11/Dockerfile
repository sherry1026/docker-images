FROM node:6.11-alpine

RUN apk update && apk add --no-cache gcc python make \
    && npm install -g cnpm --registry=https://registry.npm.taobao.org \
    && alias cnpm="npm --registry=https://registry.npm.taobao.org \
--cache=$HOME/.npm/.cache/cnpm \
--disturl=https://npm.taobao.org/dist \
--userconfig=$HOME/.cnpmrc" \
	&& npm install -g pm2
