PHPStan Contao Framework extensions and rules
=============================================

* [PHPStan](https://github.com/phpstan/phpstan)

This extension provides following features:

* Provides correct return types for Contao services.

## Usage

To use this extension, require it in [Composer](https://getcomposer.org/):

```bash
composer require --dev oneup/phpstan-contao
```

And include extension.neon in your project's PHPStan config:

```
includes:
    - vendor/oneup/phpstan-contao/extension.neon
parameters:
    contao:
        services_yml_path: %currentWorkingDirectory%/src/Resources/config/services.yml

    bootstrap: %currentWorkingDirectory%/vendor/oneup/phpstan-contao/app/bootstrap.php
```

## Limitations

You have to provide a path to `services.yml` or similar yml file describing your services.
