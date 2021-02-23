FROM node:14.15.5-alpine as builder
WORKDIR /app
COPY package.json /app
RUN npm install
COPY . /app
RUN npm run build --prod
FROM nginx:alpine
RUN rm -rf /usr/share/nginx/html/*
COPY nginx.conf /etc/nginx/nginx.conf
COPY --from=builder app/dist/frontend /usr/share/nginx/html
EXPOSE 4200
