FROM nginx

RUN rm -fr /usr/share/nginx/html/*
ADD default.conf /etc/nginx/conf.d/default.conf
ADD src /usr/share/nginx/html/
