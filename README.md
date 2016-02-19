# Docker Fumes #

## Containers ##
* Proxy
* Centos:7, Nginx, PHP56, Php-Fpm
* MariaDb:latest


## Install Docker ##

```
https://docs.docker.com/engine/installation/
```

## Install Docker-Compose ##

```
https://docs.docker.com/compose/install/
```

## Install PHP Dependencies to run ##

```
sudo apt-get install php5-cli php5-dev php5-curl
```

## To Run ##

### start ###

First time

```
docker-compose build
```

### Up machines ###
```
docker-compose up -d
```

### Stop ###
```
docker-compose stop
docker-compose rm
```
## To Run Mysql Client ##

```
mysql -uroot -proot -hdatabase.dev
```

## Web Address ##

```
webproject.dev
database.dev
```
