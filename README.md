[![Build Status](https://travis-ci.org/zackkitzmiller/tiny-php.png?branch=master)](https://travis-ci.org/zackkitzmiller/tiny-php)

# Tiny

A reversible base62 ID obfuscater

## Authors

Originally by Jacob DeHart, with Ruby and Python ports by Kyle Bragger

Now maintained by [Zack Kitzmiller](https://github.com/zackkitzmiller).

## Installation

Install via Composer

```json
{
    "require": {
        "zackkitzmiller/tiny": "1.0.1"
    },
}
```

## Usage

```php
$tiny = new \ZackKitzmiller\Tiny('5SX0TEjkR1mLOw8Gvq2VyJxIFhgCAYidrclDWaM3so9bfzZpuUenKtP74QNH6B');

echo $tiny->to(5);
// echos E

echo $tiny->from('E');
// echos 5
```

## Configuration

You must instanciate a new instance of Tiny with a random alpha-numeric set. Do **NOT** change this once you start using Tiny, as you won't be able to reverse.

## Using laravel?

If you're using laravel and want to use a more laravel-like syntax you could use [this fork](https://github.com/golonka/tiny) which will allow you to use a syntax like this:
```php
echo Tiny::to(5);
// echos E

echo Tiny::from('E');
// echos 5
```
