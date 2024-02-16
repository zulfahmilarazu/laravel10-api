# laravel10-api
 Learn Restful API development with Laravel 10 through a comprehensive repository. Perfect for understanding CRUD operations and API authentication. Based on tutorials by santrikoding.com. Link: https://santrikoding.com/tutorial-restful-api-laravel-10-1-install-laravel-10

create a new laravel 10 project named (for example) laravel10-api:
*composer create-project --prefer-dist laravel/laravel:^10.0 laravel10-api

After finished the project installation:
because of the images upload activity, its need to make a new link folder: from storage/app/public to public folder. So, execute this command on terminal:
*php artisan storage:link

then it will get results like below:
*The [public/storage] link has been connected to [storage/app/public]

make a new API Resource file named (for example) PostResource.php:
*php artisan make:resource PostResource

change the .env file
*from:
    DB_DATABASE=laravel
    DB_USERNAME=root 
    DB_PASSWORD=
*to:
    DB_DATABASE=db_laravel10_api
    DB_USERNAME=root
    DB_PASSWORD=

create a new table named:
*db_laravel10_api

execute this commands below:
*php artisan make:model Post -m
If it's haven't created the db_laravel10_api database, then select Yes to create a new database with the name db_laravel10_api

generate all (database) tables and fields from Migration file:
*php artisan migrate

create a new controller file named PostController
*php artisan make:controller Api/PostController

view the list of available route
*php artisan route:list