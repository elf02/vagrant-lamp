# LAMP stack

* hashicorp/bionic64
* Apache
* mysql 5.7 (PW: root/root)
* php 7.4
* Redis
* node 12, composer
* git, curl...

[Installing MailHog for Ubuntu 16.04](https://www.lullabot.com/articles/installing-mailhog-for-ubuntu-1604)

Timezone for Ubuntu & PHP
* sudo timedatectl set-timezone Europe/Berlin
* php.ini -> date.timezone = "Europe/Berlin"

Optional
* disable OPCache -> opcache.ini -> opcache.enable=0
