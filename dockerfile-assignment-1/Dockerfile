FROM node:6-alpine
RUN apk add --no-cache tini
WORKDIR /usr/bin/app
COPY package.json .
RUN npm install && npm cache clean --force
COPY . .
EXPOSE 3000
CMD ["/sbin/tini","--","node","./bin/www"]