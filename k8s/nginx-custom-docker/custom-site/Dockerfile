#  Every RUN, COPY, etc. in a Dockerfile adds another layer on top of the base image (nginx in this case). 
#  So this Dockerfile is “adding a layer on top of nginx”.
FROM nginx:alpine

COPY index.html /template/index.html
COPY nginx.conf /etc/nginx/nginx.conf

RUN apk add --no-cache gettext && \
    mkdir -p /usr/share/nginx/html && \
    envsubst < /template/index.html > /usr/share/nginx/html/index.html
