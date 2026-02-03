# Platform-Based Application Development - Week 5

This project is part of the Platform-Based Application Development (ABP) course, focusing on Laravel framework implementation and best practices.

<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

## About Laravel

Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable and creative experience to be truly fulfilling. Laravel takes the pain out of development by easing common tasks used in many web projects, such as:

-   Basic Laravel routing and controllers
-   Database interactions using Laravel's Eloquent ORM
-   Implementation of REST API endpoints
-   Authentication and authorization systems
-   Frontend integration using Blade templating

## Learning Laravel

For learning more about Laravel and this project:

-   [Laravel Documentation](https://laravel.com/docs)
-   [Laracasts](https://laracasts.com)
-   [Laravel News](https://laravel-news.com)

## Installation Guide

### Prerequisites

Ensure your system meets the following requirements:

-   **PHP**: Version **8.2 to 8.4**
-   **Composer**: PHP dependency manager

For additional details, refer to the [Laravel Server Requirements](https://laravel.com/docs/11.x/deployment#server-requirements).

### Installation Steps

1. **Install PHP, Composer, and Laravel Installer**

    - For Windows users, run this PowerShell command for quick setup:
        ```powershell
        Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://php.new/install/windows/8.4'))
        ```
    - For other platforms, follow the official installation guides for [PHP](https://www.php.net/manual/en/install.php) and [Composer](https://getcomposer.org/download/).

2. **Clone the Repository**

    ```bash
    git clone https://github.com/filzarahma/W5_ABP.git
    cd W5_ABP
    ```

3. **Install Dependencies**

    ```bash
    composer install
    composer update
    ```

4. **Environment Configuration**

    ```bash
    cp .env.example .env
    php artisan key:generate
    ```

    - Update the `.env` file with your database credentials and other settings.

5. **Start Development Server**
    ```bash
    composer run dev
    ```

The application will be available at [http://localhost:8000](http://localhost:8000).

### Advanced Configuration

For advanced setup options and deployment configurations, consult the official [Laravel Configuration Documentation](https://laravel.com/docs/11.x/configuration).

## About This Project

This Week 5 ABP project implements basic Laravel concepts and includes the following components:

### Project Structure

#### Routes (`/routes/web.php`)

```php
Route::get('/', function () {
    return view('welcome');
});

Route::get('/lat1', [Lat1Controller::class, 'index']);
Route::get('/lat1/m2', [Lat1Controller::class, 'method2']);
```

#### Controller (`/app/Http/Controllers/Lat1Controller.php`)

The controller implements two methods:

-   `index()`: Returns a simple view with name and origin
-   `method2()`: Returns a view with a table of student data

#### Views

1. **Basic View** (`/resources/views/v_latihan1.blade.php`)

    - Displays name and origin data
    - Uses Blade templating syntax

2. **Table View** (`/resources/views/v_latihan2.blade.php`)
    - Displays a table of students
    - Implements Blade foreach loop
    - Includes basic HTML structure with dynamic data

### Features Demonstrated

-   Route definition and handling
-   Controller implementation
-   Blade template usage
-   Data passing to views
-   Basic table rendering
-   PHP array manipulation

## Acknowledgments

-   Laravel Framework Team
-   Course Instructors and Teaching Assistants
