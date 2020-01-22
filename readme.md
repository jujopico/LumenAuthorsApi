# Lumen PHP Framework

[![Build Status](https://travis-ci.org/laravel/lumen-framework.svg)](https://travis-ci.org/laravel/lumen-framework)
[![Total Downloads](https://poser.pugx.org/laravel/lumen-framework/d/total.svg)](https://packagist.org/packages/laravel/lumen-framework)
[![Latest Stable Version](https://poser.pugx.org/laravel/lumen-framework/v/stable.svg)](https://packagist.org/packages/laravel/lumen-framework)
[![Latest Unstable Version](https://poser.pugx.org/laravel/lumen-framework/v/unstable.svg)](https://packagist.org/packages/laravel/lumen-framework)
[![License](https://poser.pugx.org/laravel/lumen-framework/license.svg)](https://packagist.org/packages/laravel/lumen-framework)

Laravel Lumen is a stunningly fast PHP micro-framework for building web applications with expressive, elegant syntax. We believe development must be an enjoyable, creative experience to be truly fulfilling. Lumen attempts to take the pain out of development by easing common tasks used in the majority of web projects, such as routing, database abstraction, queueing, and caching.

## Official Documentation

Documentation for the framework can be found on the [Lumen website](https://lumen.laravel.com/docs).

## Security Vulnerabilities

If you discover a security vulnerability within Lumen, please send an e-mail to Taylor Otwell at taylor@laravel.com. All security vulnerabilities will be promptly addressed.

## License

The Lumen framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).

# LumenAuthorsApi

## Study Notes

* Install php 7.1.3.2
* Install Composer
* Create a project `composer create-project laravel/lumen ...`
* Check on Postman or `php -S localhost:8000 -t public/` -> localhost:8000
* Enable Facades and Eloquent
* Use sqlite on databases
* Add APP_KEY (http://www.unit-conversion.info/texttools/random-string-generator/)
* Create a database migration file `php artisan make:migration CreateAuthorsTable --create=authors` 
  -> check & edit schema -> `php artisan migrate`
* Create author model with attributes -> rename `app/User.php` as `app/Author.php`
* Create factory with Faker 
  `php artisan db: seed` and `php artisan migrate:fresh --seed`
* Create author controller with 5 actions (index, store, show, update, destroy)
* Create routes for CRUD operations on the authors(get/post/get/put+patch/delete)
* Normalize author's micro-service response with reusable `Trait`
* Show the list of authors from the Lumen Controller on Postman
  -> Change `return $authors` into `return $this->successResponse($authors)` put the same authors into "data" root element
* Show an author with an given id by calling `findOrFail()` and output with `successResponse()`


