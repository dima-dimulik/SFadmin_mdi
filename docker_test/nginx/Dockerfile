# Ubuntu base image
FROM ubuntu:20.04
#Update packages & Install the nginx package
RUN apt-get update && apt-get install -y nginx
#Copy layout mysite.conf
COPY ./conf/site.conf /etc/nginx/sites-enabled/default
#Setting the working directory /data All commands will continue to work from here
WORKDIR /data
#Create the /data directory that happened when the container was restarted
VOLUME /data
# Instruction - the application runs on port 80
EXPOSE 80
# The command to start nginx when starting the container
CMD [ "nginx" , "-g" , "daemon off;" ]
