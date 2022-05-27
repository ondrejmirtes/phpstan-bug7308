# reproducer bug 7332

this repo reproduces the ~~2nd bug mentioned in https://github.com/phpstan/phpstan/issues/7308#issuecomment-1139330531~~ [bug 7332](https://github.com/phpstan/phpstan/issues/7332#issue-1251098982)

# how to reproduce

- clone the repo
- run `composer install`
- run `vendor/bin/phpstan analyze -c app/phpstan.neon  --debug`
-> everything green

update `composer.json` to use `"phpstan/phpstan": "1.6.9"` or 1.7.x

- run `vendor/bin/phpstan analyze -c app/phpstan.neon  --debug`
-> error: `Class MyApp extends unknown class ApplicationController`
