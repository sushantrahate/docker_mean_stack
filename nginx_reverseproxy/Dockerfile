FROM nginx:1.19.7
RUN apt-get update && apt-get install -y nginx-extras
COPY nginx.conf /etc/nginx/nginx.conf

EXPOSE 80