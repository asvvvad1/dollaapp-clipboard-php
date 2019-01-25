# Clipboard for PHP
Provide copying and pasting to the Clipboard for PHP.

PHP port of [atotto/clipboard](https://github.com/atotto/clipboard)

Platforms:

* OSX
* Linux, Unix (requires 'xclip' or 'xsel' command to be installed)
* Windows **not tested** (but probably work)

## Usage

```bash
composer require asvvvad/dollaapp-clipboard-php:dev-master
```

```php
require 'vendor/autoload.php';

use dollaapp\Clipboard;

$c = new Clipboard();

if ($c->isUnsupported() === false) {
	$c->writeAll('copied');
	echo $c->readAll(); // "copied"
}

```
