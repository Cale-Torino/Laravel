# Laraval setup on Windows

Watch this video for a full project https://www.youtube.com/watch?v=HKJDLXsTr8A

https://www.youtube.com/watch?v=dG55U27oSb4

https://www.youtube.com/watch?v=X4KElZcUi-g

https://laravel.com/docs/8.x/installation#getting-started-on-windows

https://www.youtube.com/watch?v=NdL-sbjIaOI

## STEPS

1. Make sure `XAMPP` is installed and running with `PHP` and `MySQL` services installed

[<img src="img/xampp.jpg" width="500"/>](img/xampp.jpg)

Also make sure NodeJS is installed https://nodejs.org/en/download

Check if node LTS version of nodejs `node -pe process.release.lts`.

```
node --version

node -pe process.release.lts
```

[<img src="img/node.jpg" width="500"/>](img/node.jpg)

2. Now download and run the windows composer `Composer-Setup.exe` file
```
https://getcomposer.org/download/
```
Make sure to select the PHP executable in your `XAMPP` folder

[<img src="img/composer.jpg" width="500"/>](img/composer.jpg)

3. Make the folder `C:\Software\xampp\htdocs\Laraval-projects`

4. CD into dir
```
cd C:\Software\xampp\htdocs\Laraval-projects
```

[<img src="img/composer_version.jpg" width="500"/>](img/composer_version.jpg)

5. Installation Via Composer 
```
composer create-project laravel/laravel iq-blueapp --prefer-dist

cd iq-blueapp

php artisan serve

```

Or, you may install the Laravel Installer as a global Composer dependency
```
composer global require laravel/installer

laravel new iq-blueapp

cd iq-blueapp

php artisan serve

```

6. Run server commands

```
CD C:\Software\xampp\htdocs\Laraval-projects\iq-blueapp

php artisan serve

php artisan serve --host 0.0.0.0 --port 8000
```

http://127.0.0.1:8000/

Laravel v8.77.0 (PHP v8.0.11)

START_SERVER.bat batch file
```BAT
::START SERVER
@ECHO OFF
:: php artisan serve
:: php artisan serve --host 0.0.0.0 --port 8000
start cmd /k php artisan serve
pause
```

## Setting up Tailwind CSS

https://www.youtube.com/watch?v=HKJDLXsTr8A&t=3333s

1. Get Tailwind presets
```
cd C:\Software\xampp\htdocs\Laraval-projects\test-app
composer require laravel-frontend-presets/tailwindcss --dev
```

2. Laraval auth
```
php artisan ui tailwindcss --auth
```

3. remove old mix
```
npm remove laravel-mix
```

4. install new mix
```
npm install laravel-mix --save-dev
```

5. install npm
```
npm install cross-env --save-dev
```

5. keep css compiling everytime tailwind is used
```
npm run watch
```

## Make controller

1. create pages controller in `C:\Software\xampp\htdocs\Laraval-projects\test-app\app\Http\Controllers` `PagesController.php`
```
php artisan make:controller PagesController
```

## Routes

`C:\Software\xampp\htdocs\Laraval-projects\test-app\routes` `web.php`

1. list routes that are made (shows all the routes that `php artisan ui tailwindcss --auth` made)
```
php artisan route:list
```
## Views

create nex view file `index.blade.php` in dir `C:\Software\xampp\htdocs\Laraval-projects\test-app\resources\views`

