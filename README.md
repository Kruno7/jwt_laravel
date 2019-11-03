# jwt_laravel
Using JWT Auth in Laravel

Install via composer
Run the following command to pull in the latest version:

composer require tymon/jwt-auth

Generate secret key
I have included a helper command to generate a key for you:

php artisan jwt:secret

Configure Auth guard

Inside the config/auth.php file you will need to make a few changes to configure Laravel to use the jwt guard to power your application authentication.

Make the following changes to the file:

'defaults' => [
    'guard' => 'api',
    'passwords' => 'users',
],

...

'guards' => [
    'api' => [
        'driver' => 'jwt',
        'provider' => 'users',
    ],

