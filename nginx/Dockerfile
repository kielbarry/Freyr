FROM nginx:alpine

COPY ./conf/nginx.conf /etc/nginx/
COPY ./conf/fullchain.cert.pem /etc/nginx/
COPY ./conf/privkey.pem /etc/nginx/

RUN mkdir -p /usr/share/nginx/html/build
RUN mkdir -p /usr/share/nginx/html/css
RUN mkdir -p /usr/share/nginx/html/js
RUN mkdir -p /usr/share/nginx/html/font-awesome
RUN mkdir -p /usr/share/nginx/html/img
COPY ./static/index.html /usr/share/nginx/html
COPY ./static/build/bundle.js /usr/share/nginx/html/build
COPY ./static/js/jquery.js /usr/share/nginx/html/js
COPY ./static/js/bootstrap.min.js /usr/share/nginx/html/js
COPY ./static/js/jquery.easing.min.js /usr/share/nginx/html/js
COPY ./static/js/grayscale.js /usr/share/nginx/html/js
COPY ./static/css/ /usr/share/nginx/html/css/
COPY ./static/font-awesome/ /usr/share/nginx/html/font-awesome/
COPY ./static/img/ /usr/share/nginx/html/img/
