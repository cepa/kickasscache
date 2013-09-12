# KickAssCacheApc

### Da fuq is this?
This is a simple caching class based on php-apc that allows your php application boot performance many times. 
It has a builtin simple mutex implementation to avoid race condition issues with multiple concurrent request, that could possibly overload your server.
***

### How it works?
Idea is very simple, when a new request is comming, hold all concurrent request to the same resource (mutex), let only one to execute and send the same result to all other request.
This way you can greatly decrease your sever load.
***

### Example
Put following code at the beginning of your index.php
~~~ php
require 'KickAssCacheApc.php';
$cache = new KickAssCacheApc();
$cache->capturePage();
~~~
***

### Support
The *KickAssCacheApc* work with any framework including ZF2, Symfony2, etc.
It is strongly recommended to use this class on nginx + php-fpm based hosting.
***

### Testing
KickAssCacheApc was testes against following versions of php:
- PHP 5.2.x
- PHP 5.3.x
- PHP 5.4.x
***

## Benchmark
More in benchmark.txt
***
