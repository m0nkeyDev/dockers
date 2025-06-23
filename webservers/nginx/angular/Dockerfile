FROM nginx:latest

COPY nginx.conf /etc/nginx/nginx.conf

COPY dist/angular001 /usr/share/nginx/html

RUN mkdir -p /etc/nginx/ssl/
COPY certs/fullchain.pem /etc/nginx/ssl/smmwebsite.com.crt
COPY certs/privkey.pem /etc/nginx/ssl/smmwebsite.com.key

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]