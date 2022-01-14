# Path converter

[![Build status](https://api.travis-ci.org/kadokweb/path-converter.svg?branch=master)](https://travis-ci.org/kadokweb/path-converter)
[![Code coverage](http://img.shields.io/codecov/c/github/kadokweb/path-converter.svg)](https://codecov.io/github/kadokweb/path-converter)
[![Code quality](http://img.shields.io/scrutinizer/g/kadokweb/path-converter.svg)](https://scrutinizer-ci.com/g/kadokweb/path-converter)
[![Latest version](http://img.shields.io/packagist/v/kadokweb/path-converter.svg)](https://packagist.org/packages/kadokweb/path-converter)
[![Downloads total](http://img.shields.io/packagist/dt/kadokweb/path-converter.svg)](https://packagist.org/packages/kadokweb/path-converter)
[![License](http://img.shields.io/packagist/l/kadokweb/path-converter.svg)](https://github.com/kadokweb/path-converter/blob/master/LICENSE)

## Usage

```php
use KadokWeb\PathConverter\Converter;

$from = '/css/imports/icons.css';
$to = '/css/minified.css';

$converter = new Converter($from, $to);
$result = $converter->convert('../../images/icon.jpg');
// $result is now '../images/icon.jpg'
```

## Methods

### \_\_construct($from, $to)

The object constructor accepts 2 paths: the source path your file(s) is/are
currently relative to, and the target path to convert to.

### convert($path): string

$path is the relative file, which is currently relative to $from (in
constructor). The return value will be the relative path of this same file, but
now relative to $to (in constructor)

## Installation

Simply add a dependency on kadokweb/path-converter to your composer.json file if you use [Composer](https://getcomposer.org/) to manage the dependencies of your project:

```sh
composer require kadokweb/path-converter
```

```bash
"kadokweb/path-converter": "1.0.*"
```

Although it's recommended to use Composer, you can actually include these files anyway you want.

## License

PathConverter is [MIT](http://opensource.org/licenses/MIT) licensed.
