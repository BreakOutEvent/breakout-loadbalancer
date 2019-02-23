# breakout-loadbalancer
A loadbalancer config for all services

## Setup on Ubuntu

 - install nginx and [certbot](https://certbot.eff.org/lets-encrypt/ubuntubionic-nginx)
 - request needed certificated for all domains using `sudo certbot --nginx`
 - clone this repository on remote
 - symlink sites-available `sudo ln -s /folder/of/repository/nginx/sites-available /etc/nginx/sites-available` then symlink sites-enabled `sudo ln -s /etc/nginx/sites-available /etc/nginx/sites-enabled`
 - check nginx config `sudo nginx -t` eventually adjust `ssl_certificate` and `ssl_certificate_key` paths
 - restart nginx `sudo systemctl restart nginx.service`
