Welcome to Bantenprov/laravel-api-manager!
===================

Documents
-------------

Ini adalah package yang di gunakan untuk laravel api manager pemprov banten, dan package ini masih versi beta, found some bugs, text me at 085711511295 or drop email to ahmadnorin@gmail.com


> **Note:**

> - Package ini masih dalam tahap pengembangan.
> - package ini di gunakan untuk sso app provinsi banten.
> - Package ini untuk laravel 4.2 keatas.

#### <i class="icon-file"></i> Install package

```sh
composer require bantenprov/laravel-api-managerL:dev-master
```
#### <i class="icon-file"></i> edit file config/app.php

tambahan class ini pada file config/app.php
```sh
Bantenprov\LaravelApiManager\LaravelApiManagerServiceProvider::class,
```

#### <i class="icon-file"></i> running script vendor:publish

running vendor publish
```sh
php artisan vendor:publish
```

hasilnya kegini
```sh
Copied Directory [/vendor/bantenprov/laravel-api-manager/src/config] To [/config]
Copied Directory [/vendor/bantenprov/laravel-api-manager/src/views] To [/resources/views/api_manager]
Copied Directory [/vendor/bantenprov/laravel-api-manager/src/controller] To [/app/Http/Controllers]
Copied Directory [/vendor/bantenprov/laravel-api-manager/src/models] To [/app]
Copied Directory [/vendor/bantenprov/laravel-api-manager/src/migrations] To [/database/migrations]
Copied Directory [/vendor/laravel/framework/src/Illuminate/Mail/resources/views] To [/resources/views/vendor/mail]
Publishing complete.
```
#### <i class="icon-file"></i> tambahkan route 

running script
```sh
php artisan laravel-api-manager:add-route
```

hasilnya akan menambahkan route resource di routes/web.php
```sh
Route::resource('api_manager', 'ApiManagerController');
```

#### <i class="icon-file"></i> Migrasi database 

running script
```sh
php artisan migrate
```

#### <i class="icon-file"></i> Running Modul 

browse dari browser anda
```sh
http://your_domain.dev/api_manager
```
#### <i class="icon-file"></i> Running Modul 

tambahkan pada .env anda parameter berikut
```sh
BANTENPROV_APIHOST=api.bantenprov.go.id
```
untuk production site
```sh
BANTENPROV_APIHOST=api-01.dev.bantenprov.go.id
```
untuk development site
#### <i class="icon-file"></i> Happy Coding  \\(*i^)//
