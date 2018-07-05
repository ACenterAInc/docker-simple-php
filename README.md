# Simple PHP for Docker

This project is a small PHP starting point. 

### Getting Started in 1 seconds

Clone this repository and run `docker-compose up` then point your browser at
`http://localhost:8080` and you should see a beautiful PHP info page.


### nginx

The Nginx website config can be edited in any editor that you like. The file is located at
`.docker/config/nginx.conf` which will be picked up on starting the container.


### PHP

The included version of PHP-FPM includes GD, Intl and BZ2 extensions as well as
Composer being installed as well.


### Accessible URLs

You can access the services Nginx, MariaDB, Mailhog and Beanstalkd Console at:

 - Nginx - http://localhost:8080


### Accessing PHP within the stack

If you're running something like Laravel and need to run `php artisan migrate`, you can
do this by running:

   `docker-compose exec php bash`

within the project directory, this will give you a bash prompt that you can then `cd /www`
and run `php artisan migrate` and it'll run the migrations.


### .gitignore

It'll be wise to add the following into your `.gitignore` file to stop the
MariaDB databases being added to your repo:

    .docker/volumes/xxx/*
    !.docker/volumes/xxx/.gitkeep

### docker-compose-acentera.yml

This are the dockers that will be executed in our docker hosting platform. See our docs.


### License

This project is licensed under an Apache 2.0 license which you can find within
this repository in the [LICENSE file](https://github.com/CenterAInc/docker-simple-php/blob/master/LICENSE).
