# GameAP Daemon Flysystem

[![Build Status](https://travis-ci.com/et-nik/flysystem-gameap.svg?branch=master)](https://travis-ci.com/et-nik/flysystem-gameap)
[![Quality Score](https://img.shields.io/scrutinizer/g/et-nik/flysystem-gameap.svg?style=flat-square)](https://scrutinizer-ci.com/g/et-nik/flysystem-gameap)
[![Coverage Status](https://scrutinizer-ci.com/g/et-nik/flysystem-gameap/badges/coverage.png?b=master)](https://scrutinizer-ci.com/g/et-nik/flysystem-gameap/code-structure)

GameAP Daemon Files Adapter 

## Installation

```bash
composer require knik/flysystem-gameap
```

## Usage

```php
use Knik\Flysystem\Gameap\GameapAdapter;
use League\Flysystem\Filesystem;

$adapter = new GameapAdapter([
    'host' => 'localhost',
    'port' => 31717,
    'username' => 'username',
    'password' => 'password',
    'privateKey' => '/path/to/private_key',
    'privateKeyPass' => 'pr1vateKeyPa$$',
    'root' => '/home/gameap',
    'timeout' => 10,
]);

$filesystem = new Filesystem($adapter);
```