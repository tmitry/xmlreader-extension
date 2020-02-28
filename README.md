# XMLParser

## About

[XMLReader](https://www.php.net/manual/ru/book.xmlreader.php) for PHP extension. 


## 1. Installation ##

Add the `tmitry/xmlreader-extension` package to your `require` section in the `composer.json` file.

``` bash
$ composer require tmitry/xmlreader-extension
```

## 2. Usage ##

```php
use tmitry\XMLReaderExtension\XMLParser;

$parser = new XMLParser();
$parser->open($fileName);

// or

$xmlReader = new XMLReader();
$xmlReader->open($fileName);
// some actions with $xmlReader
$parser = new XMLParser($xmlReader);


		
		
// use extenstion
$parser->moveTo('root/products/');
if ($parser->moveIn()) {
    do {
        // some actions
    } while ($this->parser->moveToNextSibling());
}
```
