FROM node:6.11.3

#make a app dir
RUN mkdir -p /srv/www/app

#now lets use that dir for the following commands
WORKDIR /srv/www/app

#expose port 8080 as stated from the node app, maybe should be dynamic to play nicely with the node config
EXPOSE 8080

#copy entrypoint script and set permissions so we can execute
COPY entrypoint.sh /entrypoint.sh
RUN chmod 0755 /entrypoint.sh

#run that bad boy
CMD ["/entrypoint.sh"]