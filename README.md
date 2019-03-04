# LAMP stack docker-compose config files
Docker-compose multiple container config files (YML), includes static container IP addresses, services from dockerhub (including one of my own - https://hub.docker.com/r/robertbourne/php-extras-apache).

##Installation
Alongside the docker-compose file are two directories:
###config
These docker-compose files are written to allow multiple sites to be ran through the same containers without modifying the files for each new project. To enable a new virtual host, clone and modify the `example.conf` file within the `/config/vhosts/` directory. Once you have added a new vhost, you can update your local hosts file and point the your domain to your docker container IP address (by default `172.20.0.6`). Included in this repo is specific config files for apache, mysql, php and phpmyadmin. These config could be moved into the single docker-compose file if desired.

###sites
This is the web root directory, multiple sites can be placed here. There will be slight configuration required to add a new site with a custom host. 


@todo - add drupal specific environment with extras - drush, drupal console, redis etc 
