# Команды Docker Compose
  * Стартовать (в фоне): `docker-compose up -d`
  * Стартовать: `docker-compose up`
  * Остановить: `docker-compose stop`
  * Убить: `docker-compose kill`
  * Логи : `docker-compose logs`
  * Выполнить команду внутри: `docker-compose exec SERVICE_NAME COMMAND` где `COMMAND` то что хочешь выполнить
  
    * Bash внутри контейнера, `docker-compose exec php-fpm bash`
    * Symfony console, `docker-compose exec php-fpm bin/console`
    * Mysql, `docker-compose exec mysql mysql -uroot -pCHOSEN_ROOT_PASSWORD`

# Команды Docker    
  * Удалить контейнеры: `docker rm -f $(docker ps -a -q)`
  * Удалить образы: `docker rmi -f $(docker images -a -q)`
  * Удалить volumes: `docker volume rm $(docker volume ls -q)`
  * Удалить networks: `docker network rm $(docker network ls | tail -n+2 | awk '{if($2 !~ /bridge|none|host/){ print 
 $1 }}')`
