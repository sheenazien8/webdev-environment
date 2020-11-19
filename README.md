# webdev-environment
My Dev Setup

## PHP
### Install Lemp Stack
  * Nginx
    * sudo apt update
    * sudo apt install nginx
    * sudo ufw app list
      ```
      Output
      Available applications:
        Nginx Full
        Nginx HTTP
        Nginx HTTPS
        OpenSSH
      ```
    * sudo ufw allow 'Nginx HTTP'
    * sudo ufw status
      ```
      Output
      Status: active

      To                         Action      From
      --                         ------      ----
      OpenSSH                    ALLOW       Anywhere
      Nginx HTTP                 ALLOW       Anywhere
      OpenSSH (v6)               ALLOW       Anywhere (v6)
      Nginx HTTP (v6)            ALLOW       Anywhere (v6)
      ```
  * Mysql
    * sudo apt install mysql-server
    * sudo mysql_secure_installation
    * sudo mysql
    * mysql> exit
  * PHP -> Latest Version
    * sudo apt install php-fpm php-mysql
### Install Laravel Stack
  * Composer
    * sudo apt install curl php-cli php-mbstring git unzip
    * cd ~ && curl -sS https://getcomposer.org/installer -o composer-setup.php
    * Verify SHA-384 for Composer public key 'HASH=544e09ee996cdf60ece3804abc52599c22b1f40f4323403c44d44fdfdd586475ca9813a858088ffbc1f233e9b180f061'
    * php -r "if (hash_file('SHA384', 'composer-setup.php') === '$HASH') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
      ```
      Installer verified
      ```
    * sudo php composer-setup.php --install-dir=/usr/local/bin --filename=composer
      ```
      Output
      All settings correct for using Composer
      Downloading...

      Composer (version 1.6.5) successfully installed to: /usr/local/bin/composer
      Use it: php /usr/local/bin/composer
      ``
    * composer global bin
      ```
      /home/sheenazien/.config/composer
      ```
    * export PATH=~/.config/composer/vendor/bin:$PATH
    * composer
      ```
      Output
         ______
        / ____/___  ____ ___  ____  ____  ________  _____
       / /   / __ \/ __ `__ \/ __ \/ __ \/ ___/ _ \/ ___/
      / /___/ /_/ / / / / / / /_/ / /_/ (__  )  __/ /
      \____/\____/_/ /_/ /_/ .___/\____/____/\___/_/
                          /_/
      Composer version 1.6.5 2018-05-04 11:44:59
      ```
  * Valet
    * composer global require cpriego/valet-linux
    * valet install
  * Laravel
    * sudo apt install php libapache2-mod-php php-common php-mbstring php-xmlrpc php-soap php-gd php-xml php-mysql php-cli php-mcrypt php-zip
    * composer global require laravel/installer
      ```
      Laravel Installer 3.0.1
      Usage:
        command [options] [arguments]

      Options:
        -h, --help            Display this help message
        -q, --quiet           Do not output any message
        -V, --version         Display this application version
            --ansi            Force ANSI output
            --no-ansi         Disable ANSI output
        -n, --no-interaction  Do not ask any interactive question
        -v|vv|vvv, --verbose  Increase the verbosity of messages: 1 for normal output, 2 for more verbose output and 3 for debug

      Available commands:
        help  Displays help for a command
        list  Lists commands
        new   Create a new Laravel applicatio
      ```
## Javascript
    
