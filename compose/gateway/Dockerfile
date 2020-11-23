FROM nginx:1.13.3-alpine-perl

RUN apk add --no-cache apache2-utils openssl vim

COPY nginx.conf /etc/nginx/nginx.conf
COPY entrypoint /usr/local/bin/entrypoint
RUN ["chmod", "+x", "/usr/local/bin/entrypoint"]

EXPOSE 80 443

ENTRYPOINT [ "/usr/local/bin/entrypoint" ]
CMD ["nginx", "-g", "daemon off;"]
