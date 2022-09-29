# Оглавление

- [301 редирект][1]

**.htaccess** — это конфигурационный файл веб-сервера Apache, позволяющий управлять работой веб-сервера и настройками сайта с помощью различных параметров (директив) без изменения основного конфигурационного файла веб-сервера.
#htaccess

***
[1]
# 301 редирект

    RewriteCond %{HTTP_HOST} ^www\.(.*)$
    RewriteRule ^(.*)$ http://%1/$1 [L,R=301]
    
    RewriteCond %{HTTPS} off
    RewriteCond %{HTTP:X-Forwarded-Proto} !https
    RewriteRule ^(.*)$ https://%{HTTP_HOST}%{REQUEST_URI} [L,R=301]


#htaccess/301
#htaccess/301/www
#htaccess/301/https
