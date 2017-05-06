### CREATE MY SQL DATABASE

```
mysql -u {database user name} -p

CREATE USER 'betman'@'localhost' IDENTIFIED BY '{database paswprd}';  // ignor {} bracket
GRANT ALL PRIVILEGES ON * . * TO '{database name}'@'localhost';

SHOW DATABASES;
CREATE DATABASE {database name};
DROP DATABASE {database name};
USE events;
SHOW tables; 
```
### CONFIG NEW SITE ON NGINX 
```
cd /etc/nginx/sites-available/
sudo nano digitalocean -> change localhost to domain name
sudo service nginx reload
```
### COPY DEFUALT CONFIG FILE digitalocean INTO NEW WEB
```
sudo cp {digitablocean} {newName} 
# FOR LARAVEL ADD IN EROOR 404 /index.php?$query_string;
```
### ENABLE NEW SITE
```
sudo ln -s /etc/nginx/site-avilable/{name} /etc/nginx/site-enabled/{name} 
sudo service nginx restart
```
## LARAVEL SETTING
```
sudo chmod -R 777 storage

APP_ENV=local
APP_DEBUG=true
in prod you set

APP_ENV=production
APP_DEBUG=false
```
### INSTALLING PHPMYADMIN & CONFIG
```
sudo apt-get update
sudo apt-get install phpmyadmin

Then copy paste just before the last } of the file the following block into /etc/nginx/sites-avaliable/default

location /phpmyadmin {
        root /usr/share/;
        index index.php index.html index.htm;
        location ~ ^/phpmyadmin/(.+\.php)$ {
            try_files $uri =404;
            fastcgi_pass unix:/var/run/php/php7.0-fpm.sock;
            include fastcgi_params;
            fastcgi_param SCRIPT_FILENAME $document_root$fastcgi_script_name;

        }
        location ~* ^/phpmyadmin/(.+\.(jpg|jpeg|gif|css|png|js|ico|html|xml|txt))$ {
            root /usr/share/;
        }
    }

sudo service nginx restart
```
