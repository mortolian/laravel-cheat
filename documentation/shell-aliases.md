# Shell Aliases

If you are are using Unix, Linux or Mac these shell aliases can be handy to have around.

## Composer

```shell
# Composer new project
alias claravel='composer create-project laravel/laravel'
```

Or, you may create new Laravel projects by globally installing the Laravel installer via Composer:

```shell
composer global require laravel/installer
laravel new example-app
```

[Laravel Installation](https://laravel.com/docs/10.x/installation)

## Laravel Artisan

```shell
# Laravel Sail Shortcut
alias art='[ -f artisan ] && php artisan.php'
```

## Laravel Sail

```shell
# Laravel Sail Shortcut
alias sail='[ -f sail ] && sail ||  vendor/bin/sail'
```

[Sail Documentation](https://laravel.com/docs/10.x/sail)

## Laravel Pint

```shell
# Laravel Pint - Normal fix behaviour
alias pint-fix='[ -f pint ] && pint || vendor/bin/pint'
```

```shell
# Laravel Pint - Only display problems
alias pint-fix='[ -f pint ] && sh pint --test -v || sh vendor/bin/pint --test -v'
```

[Pint Documentation](https://laravel.com/docs/10.x/pint)
