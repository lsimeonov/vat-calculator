VatCalculator
================

[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE.md)
[![Build Status](https://travis-ci.org/mpociot/vat-calculator.svg)](https://travis-ci.org/mpociot/vat-calculator)
[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/mpociot/vat-calculator/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/mpociot/vat-calculator/?branch=master)
[![SensioLabsInsight](https://insight.sensiolabs.com/projects/adecb98a-8484-48cb-be13-803decc475bc/mini.png)](https://insight.sensiolabs.com/projects/adecb98a-8484-48cb-be13-803decc475bc)

VAT / Tax calculation for Laravel 5. Fully compatible with the new EU MOSS reverse charge processing.

```php
// Easy to use!
VatCalculator::calculate( 24.00, 'DE' );
VatCalculator::calculate( 71.00, 'DE', $isCompany = true );
VatCalculator::getTaxRateForCountry( 'NL' );
```

## Installation

In order to install the VAT Calculator, just run

```bash
$ composer require mpociot/vat-calculator
```

Then in your `config/app.php` add 

    Mpociot\VatCalculator\VatCalculatorServiceProvider::class
    
in the `providers` array.
    
The `VatCalculator` Facade will be installed automatically within the Service Provider.

<a name="configuration"/>
## Configuration

To publish the configuration files, run the `vendor:publish` command

```bash
$ php artisan vendor:publish --provider="Mpociot\VatCalculator\VatCalculatorServiceProvider"
```

This will create a `vat_calculator.php` in your config directory.
This configuration holds all EU relevant tax rules.

## Changelog
Please see [CHANGELOG](CHANGELOG.md) for more information.

## Running Tests
``` bash
$ composer test
```

## License
This library is licensed under the MIT license. Please see [License file](LICENSE.md) for more information.
