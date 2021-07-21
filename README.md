### Init env variables
cp .env.example .env

------------------
### Clone Project
Place project from https://github.com/gradyskyi/laravel-for-tig in neighbor folder

------------------
### Run docker-compose stack
docker-compose up -d nginx mongo elasticsearch grafana influxdb telegraf

------------------
### Execute to workspace
docker-compose exec workspace bash
### and run
composer install
php artisan migrate

------------------
### Create Influx batabase
echo "curl -XPOST 'http://localhost:8086/query' --data-urlencode 'q=CREATE DATABASE telegraf'"

------------------
### Load laravel project 
http://localhost/api/create-user

------------------
### Go to grafana (with admin/admin creds):
http://localhost:3000/
