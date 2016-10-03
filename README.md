# MVLabs Coding Standards for php-cs

This is a custom sniff for [PHP_CodeSniffer](http://pear.php.net/PHP_CodeSniffer) that tries to allow the use of PSR-2 standards together with the newer PHP 7 features.

- [Prerequisities](#prerequisities)
- [Install](#install)
- [Usage](#usage)


### Prerequisites

[PHP_CodeSniffer](http://pear.php.net/PHP_CodeSniffer) must be installed with the default "standards".

## Install

Add this repository to your project composer.json:
~~~~
"repositories": [
        {
            "url": "https://git.mvlabs.it/andrea/coding-standard.git",
            "type": "git"
        }
    ]
~~~~

require the package in your dev dependencies:
~~~~
php composer-phar require --dev mvlabs/coding-standard:dev-master
~~~~


## Usage
You should copy the template `vendor/mvlabs/code-standard/phpcs.xml.dist`
in your root directory with the name `phpcs.xml`, edit it accordingly, and set your code sniffer to read rules from there:

If you run PHP_CodeSniffer without specifying a coding standard, 
PHP_CodeSniffer will look in the current directory and all parent directories for a file called phpcs.xml, so it will automatically adapt to the new standard.

If you use an IDE you have to configure it accordingly:
In PHP Storm you should go in `File -> Settings -> Editor -> Inspections -> PHP -> PHP Code Sniffer Validation -> Coding Standard`
from the dropdown menu select Custom and then point to the phpcs.xml file in your project.




