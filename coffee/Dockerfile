# Use an official NGINX image as the base image
FROM nginx:mainline-alpine3.18-slim

# Remove the default NGINX configuration
#RUN rm -f /etc/nginx/conf.d/default.conf

# Copy your HTML and CSS files to the NGINX default web server directory
COPY . /usr/share/nginx/html


WORKDIR /usr/share/nginx/html

# Expose port 80 for web traffic
EXPOSE 81

RUN chmod -R +r /usr/share/nginx/html

RUN chmod -R 755 /usr/share/nginx/html

# Start NGINX in the foreground
CMD ["nginx", "-g", "daemon off;"]
