# Swoole IDE Helper

[![Latest Stable Version](http://img.shields.io/packagist/v/nizerin/swoole-ide-helper.svg)](https://packagist.org/packages/nizerin/swoole-ide-helper)
[![Packagist](https://img.shields.io/packagist/dt/nizerin/swoole-ide-helper)](https://packagist.org/packages/nizerin/swoole-ide-helper)

Add IDE helper for the **swoole** extension, forked from [swoole/ide-helper](https://github.com/swoole/ide-helper)

> `nizerin/swoole-ide-helper` keep the same version of **swoole**

## Diff With swoole/ide-helper

Different from the source repository: variable types are added to most method parameters for easy reference. 

Old：

```php
/**
 * @param $fd
 * @param $data
 * @param $opcode
 * @param $finish
 * @return mixed
 */
public function push($fd, $data, $opcode = null, $finish = null){}
```

**Now**:

```php
/**
 * @param int $fd
 * @param mixed $data
 * @param int $opcode
 * @param bool $finish
 * @return mixed
 */
public function push(int $fd, $data, int $opcode = null, bool $finish = null){}
```

## Install

You can add it by `composer`:

```bash
composer require --dev nizerin/swoole-ide-helper

# use latest code
composer require --dev nizerin/swoole-ide-helper@dev-master

```

## Build

You can regenerate it locally. Of course, you must ensure that the `swoole` extension is already installed.

```bash
php dump.php
```

## LICENSE

See [LICENSE](LICENSE)
