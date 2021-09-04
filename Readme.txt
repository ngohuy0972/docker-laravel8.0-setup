Link setup file : https://viblo.asia/p/minh-da-docker-hoa-mot-ung-dung-laravel-nhu-the-nao-naQZRyjjKvx

Folder .docker : is storage Dockerfile, data mount from container
Folder src : is storage source code laravel. You need copy source code into here.


After config done.
Step 1 : docker-compose build.
Step 2 : docker-compose up.
Step 3 : Create .env or copy from .env.example.
Step 4 : Generate key for laravel app "docker container exec laravel_workspace php artisan key:generate". (laravel_workspace is  container_name)
Step 5 : After that, you must migrate database "docker container exec laravel_workspace php artisan migrate"
Step 6 : Lauch composer to install laravel libs "docker container exec laravel_workspace composer install".
Step 7 : Allow permission for Storage folder "chmod -R 777 ./src/storage".
Step 8 : Follow link: localhost:8080.


# connect tableplus via user and password of mysql.
