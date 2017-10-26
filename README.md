# bitstorm
Fork of Bitstorm project to use PDO instead of mysql or mysqli extension

## Install
* `git clone` this repository in an accessible location on your web server
* create the `bistorm` database by executing `bitstorm.sql`
  * recommended: create specific user/password to access the database

## Configure
* create the configuration.php file in the same directory, shoule be something like:
```php
<?php
define('__DB_SERVER', '127.0.0.1'); // your mysql server host address
define('__DB_PORT', '3306'); // your mysql server port
define('__DB_NAME', 'bitstorm'); // your mysql database name
define('__DB_USERNAME', 'bitstorm'); // username to connect againt your mysql server
define('__DB_PASSWORD', 'stormbit'); // password to connect againt your mysql server
define('__DB_PERSISTENT_CONNECTION', true); // use a persistent connection (true) or not (false)
```
* hit the announce.php file in your browser http://your-tracker.url/announce.php, should return this error message:
```
d14:failure reason29:Invalid request, missing datae
```

## How to host your torrent
When you creating a torrent, use `http://your-tracker.url/announce.php` as the announce URL. Database insert and announce to other peer will be done automatically.

## Credits
Thanks to [Peter Caprioli](https://stormhub.org/tracker/) for the original project and [Josh Duff](https://github.com/TehShrike) for the original mysql support.
