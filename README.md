# Laravel Analytics

Easily collect page view analytics with a beautifully simple to use dashboard.

![Laravel Analytics Dashboard](/screenshot.png?raw=true "Laravel Analytics Dashboard")

## Installation

Install the package:

```bash
composer require andreaselia/analytics
```

Publish the configuration with the install command:

```bash
php artisan analytics:install
```

Don't forget to run the migrations:

```bash
php artisan migrate
```

You can add the page view middleware to a specific route group, e.g. `web.php` like so:

```php
Route::middleware('analytics')->group(function () {
    // ...
});
```

Or add the page view to all middlewares/on an application level like so:

```php
// app/Http/Kernel.php

protected $middleware = [
    // ...
    \AndreasElia\Analytics\Http\Middleware\Analytics::class,
];
```

## Contributing

You're more than welcome to submit a pull request, or if you're not feeling up to it - create an issue so someone else can pick it up.
