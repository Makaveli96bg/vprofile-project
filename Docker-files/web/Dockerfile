FROM nginx
LABEL "project"="vprofile"
LABEL "Author"="Imran"

# Remove the default NGINX configuration file
RUN rm -rf /etc/nginx/conf.d/default.conf

# Copy your custom NGINX configuration file
COPY nginvproapp.conf /etc/nginx/conf.d/vproapp.conf
