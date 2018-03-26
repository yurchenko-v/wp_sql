Ubuntu 16.04.4-server

Docker version 17.05.0-ce, build 89658be

Docker-compose version 1.20.1, build 5d8c71b

1. Clone repo

$git clone https://github.com/yurchenko-v/wp_sql

2. Enter to the folder
$cd wp_sql

3. Make dir & give permissions for MySQL logs files
$mkdir -p logs/mysql && sudo chown 999:999 logs/mysql/

4. On the first run, you must to initializing database
$docker-compose -f stack.yml up
Wait for message "MySQL init process done. Ready for start up."
(Then ctrl+c and $docker-compose rm)

5. Now start the all system
docker-compose up -d

Wordpress is aviable at http://localhost:8000

