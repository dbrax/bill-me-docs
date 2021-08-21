---
id: 586d4f7c-c6d5-4858-837a-fd2829e04f87
blueprint: pages
title: Installation
description: 'Bill-me package can easily be added or installed on your application'
updated_by: b5e10532-9e62-4a0b-ade2-4803339d6a5b
updated_at: 1629570942
---
This package can be used with Laravel 7.1 or higher.



1. This package publishes a config/bill-me.php file. If you already have a file by that name, you must rename or remove it.


2. You can install the package via composer:

```bash
composer require epmnzava/bill-me
```
3. After running the command you will need to publish it's configurations by running

```php

php artisan vendor:publish --provider="Epmnzava\BillMe\BillMeServiceProvider"

```

4. Optional: The service provider will automatically get registered. Or you may manually add the service provider in your config/app.php file:

```php

'providers' => [
    // ...
    Epmnzava\BillMe\BillMeServiceProvider::class,
];

```

5. Clear your config cache. This package requires access to the bill-me config. Generally it's bad practice to do config-caching in a development environment. If you've been caching configurations locally, clear your config cache with either of these commands:

```php 

 php artisan optimize:clear
 # or
 php artisan config:clear
 
 ```

6. Run the migrations: After the config and migration have been published and configured, you can create the tables for this package by running:

```php 

 php artisan migrate
 
 ```