FROM nginx:latest

RUN apt-get update && apt-get install -y apache2-utils && rm -r>

RUN echo 'admin:'$(openssl passwd -apr1 secret-passphrase) > /e>

COPY nginx.conf /etc/nginx/nginx.conf
COPY certs/server.crt /etc/nginx/ssl/server.crt
COPY certs/server.key /etc/nginx/ssl/server.key

EXPOSE 443
CMD ["nginx", "-g", "daemon off;"]