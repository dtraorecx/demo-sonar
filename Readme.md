## Gestion des droits 
chown -R www-data:www-data sf_app/var/

## lancer le container

docker-compose up -d

## generate reports

XDEBUG_MODE=coverage ./bin/phpunit --coverage-clover=var/reports/phpunit-coverage-result.xml --log-junit=var/reports/phpunit-execution-result.xml
