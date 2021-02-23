FROM node:14.15.5-alpine as builder
WORKDIR /app
COPY package.json /app
RUN npm install --silent --production
COPY . /app
CMD [ "node","server.js" ]