FROM nginx

MAINTAINER Oliver Castro <olivertamboboycastro@gmail.com>

ADD ./etc/vhost.conf /etc/nginx/conf.d/default.conf

EXPOSE 443

CMD ["nginx", "-g", "daemon off;"]