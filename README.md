# Features

- CentOS 6
- Nginx
- MariaDB 10.1
- PHP 5.6
- Phalcon 3.2.2
- Git
- AWS Command Line Interface
- Supervisor
- Unzip
- Composer

# Quickstart

```
git clone https://github.com/battcor/docker-lemp-centos-6
cd docker-lemp-centos-6/
docker build -t battcor/docker-lemp-centos-6:latest .
docker run \
    -v $(pwd)/html:/var/www/html \
    -v $(pwd)/files/default.conf:/etc/nginx/conf.d/default.conf \
    -v $(pwd)/files/supervisord.conf:/etc/supervisord.conf \
    -v $(pwd)/files/start.sh:/var/www/html/start.sh \
    --name docker-lemp-centos-6 -p 127.0.0.1:8080:80 battcor/docker-lemp-centos-6
```

Then, open http://127.0.0.1:8080 in your browser

