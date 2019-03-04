# LAMP stack docker-compose config files
Docker-compose multiple container config files (YML), includes static container IP addresses, services from dockerhub (including one of my own - https://hub.docker.com/r/robertbourne/php-extras-apache).

##Installation
Alongside the docker-compose file are a few things to setup for this environment:
###config folder 
Included in this repo is specific config files for apache, mysql, php and phpmyadmin. These config could be moved into the single docker-compose file if desired.
These docker-compose files are written to allow multiple sites to be ran through the same containers without modifying the files for each new project. To enable a new virtual host, clone and modify the `example.conf` file within the `/config/vhosts/` directory. 

###sites
This is the web root directory, multiple sites/projects can be placed here.  

###hosts file
Once you have added a new vhost, you can update your local hosts file and point the domain (host) to your docker container IP address (by default `172.20.0.6`). Included is an `example-hosts` file copy the contents into your operating systems hosts file (its location is dependant on OS).


@todo - add drupal specific environment with extras - drush, drupal console, redis etc.
@todo - add xdebug settings. 
