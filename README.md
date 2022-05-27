# reproducer bug 7308

this repo reproduces the 2nd bug mentioned in https://github.com/phpstan/phpstan/issues/7308#issuecomment-1139330531

# how to reproduce

- clone the repo
- run `composer install`
- run `vendor/bin/phpstan analyze -c app/phpstan.neon  --debug`
-> everything green

update `composer.json` to use `"phpstan/phpstan": "1.6.7"` or 1.7.x

- run `vendor/bin/phpstan analyze -c app/phpstan.neon  --debug`
-> error: `Class MyApp extends unknown class ApplicationController`