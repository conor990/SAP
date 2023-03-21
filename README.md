##creating a docker network
docker network create the_network

## mySQL docker image running
docker run -d --name db -e MYSQLROOTPASSWORD=my-secret-password mysql:latest

## running phpMyAdmin on docker network
docker run -d --name phpmyadmin -p 8080:80 --network the_network phpmyadmin/phpmyadmin

