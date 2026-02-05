FROM node:22-alpine
WORKDIR /var/www

RUN apk add --no-cache git && git config --global --add safe.directory /var/www

COPY . / /var/www

RUN npm install && npm run build

ENV SKIP_WAYFINDER=1