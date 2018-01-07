FROM ubuntu:16.04

MAINTAINER Hoanh An "hoanhan@bennington.edu"

ENV REFRESHED_AT 2018-06-01

# Install nginx
RUN apt-get -yqq update; apt-get -yqq install nginx

# Create a directory in the container
RUN mkdir -p /var/www/html/website

# Add the nginx config file to our image
ADD nginx/global.conf /etc/nginx/conf.d/
ADD nginx/nginx.conf /etc/nginx/nginx.conf

EXPOSE 80