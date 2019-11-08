# Installation Guide NGINX + PHP on Mac OS Catalina

### 1. Install Homebrew and Command Line (automatically when install homebrew): 
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

### 2. Install NGINX and PHP: 

brew install nginx php

brew install php

### 3. Add Nginx folder: 
mkdir -p /usr/local/etc/nginx/sites-{enabled,available} 

cd /usr/local/etc/nginx/sites-enabled 

ln -s ../sites-available/default.conf 

**and if using ssl then:** 

ln -s ../sites-available/default-ssl.conf

### 4. Paste config in /usr/local/etc/nginx/sites-available/default.conf

### 5. Paste config in /usr/local/etc/nginx/php-fpm.conf

### 6. Paste config in /usr/local/etc/nginx/nginx.conf

If blocked 9000 port change on file /usr/local/etc/php/7.3/php-fpm.d/*.conf in line:

listen = 127.0.0.1:9090

### 7. Start services:

brew services start php 

brew services start nginx


### Test you http://localhost. Profit 🎉
