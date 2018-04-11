# the content is in the content directory
# the configuration files are in the conf directory, 
#both subdirectories of the directory where the Dockerfile is located. 
#The NGINX image has the default NGINX configuration files, 
#including default.conf, in the /etc/nginx/conf.d directory. 
#Since we instead want to use the configuration files from the host, 
#we include RUN commands that delete the default files:

FROM nginx
RUN rm /etc/nginx/conf.d/default.conf
COPY content /var/www/html
COPY conf /etc/nginx
RUN chmod -R 755 /var/www/html/*
