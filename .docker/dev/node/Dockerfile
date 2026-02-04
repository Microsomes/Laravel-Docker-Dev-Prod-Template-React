FROM node:22-alpine
WORKDIR /var/www

COPY . / /var/www

RUN npm install && npm run build

ENV SKIP_WAYFINDER=1