title: PHP-THE-RIGHT-WAY
---

翻译整理 PHP-THE-RIGHT-WAY。 [英文原版](http://www.phptherightway.com/)的结构不舒服, [中文版](http://laravel-china.github.io/php-the-right-way/)的翻译不合胃口。 重新组织翻译, 尽可能:1保留原意2精炼概况3适度补充

## Welcome

PHP发展多年，大量过时信息误导着开发者、传播着错误实践及不安全代码。本书将为流行的PHP编程规范做一个快速参考手册，链接当下权威教程、最佳实践。

本书旨在为新手开阔眼界，为老手提供解决问题新思路。PHP没有绝对权威的用法，解决问题有多种方法、多种工具。

本书随着技术发展而持续更新有用信息及案例。

## 开始使用 

### 当前稳定版本（7.0）

当前php稳定版本为[PHP 7.0](http://php.net/downloads.php)

目前大多数项目还处于PHP 5.x， 特别是5.6。这是个不错的选择，但本书还是建议你尽快拥抱7.0。

升级不苦，7.0 没有太多[向后不兼容特性](http://php.net/manual/zh/migration70.incompatible.php)，当你不确定某个用法是否属于7.0，可以查阅官方文档[php.net](php.net/manual)

### 内置服务器（Built-in web server）
php5.4之后内置web服务器

``` bash
$ php -S localhost:8000
```
- [了解更多](http://php.net/features.commandline.webserver)

### MAC 安装PHP
OS X 自带PHP，但是通常版本稍落后。

#### Homebrew
[Homebrew](http://brew.sh/) 是 OSX 上强大的管理包管理工具，通过它可以轻松安装 PHP 及 PHP 各种拓展
用 brew install 命令安装 php53, php54, php55, php56 或 php70， 并可通过修改 PATH 环境变量切换版本
或者，可以使用 [brew-php-switcher](https://github.com/philcook/brew-php-switcher) 切换 PHP 版本

## 代码风格
pass

## 语言亮点

### 编程范式
PHP 是动态语言，支持多种编程技巧。
- PHP 5.0 (2004) 引入面向对象
- PHP 5.3 (2009) 引入匿名函数和命名空间
- PHP 5.4 (2012) 增加的 traits

#### 面向对象 Object-oriented Programming
PHP 拥有完整的面向对象编程的特性，包括类、抽象类、接口、继承、构成器、克隆、异常...
- [面向对象](http://php.net/language.oop5)
- [Traits](http://php.net/language.oop5.traits)

#### 函数式编程 Functional Programming
PHP 支持firse-class functions, 即函数可以被赋值给变量并动态调用，包括自定义函数和内置函数。函数可作为参数传递给其他函数（称为高阶函数 Higher-order Functions），也可作为函数返回值返回。
PHP 支持递归，即函数自己调用自己，但大多数使用迭代
PHP 5.3 (2009) 之后开始引入匿名函数(支持闭包)
PHP 5.4 增加了将闭包绑定到对象作用域中的特性，并改善其可调用性，大部分情况下使用匿名函数取代一般的函数
- [PHP 函数式编程](http://laravel-china.github.io/php-the-right-way/pages/Functional-Programming.html)
- [匿名函数](http://php.net/functions.anonymous)
- [闭包类](http://php.net/class.closure)
- [Closures RFC](https://wiki.php.net/rfc/closures)
- [Callables](http://php.net/language.types.callable)
- 动态调用函数 [call_user_func_array()](http://php.net/function.call-user-func-array)

#### 元编程 Meta Programming

PHP 通过反射 API 和魔术方法，可实现多种元编程。通过魔术方法，如 __get(), __set(), __clone(), __toString(), __invoke()等改变类的行为。Ruby 开发者常说 PHP 没有 `method_missing` 方法，实际上通过 __call() 和 __callStatic() 就可以完成相同的功能。
- [魔术方法](http://php.net/language.oop5.magic)
- [反射](http://php.net/intro.reflection)
- [重载](http://php.net/language.oop5.overloading)

### 命名空间 (Namespaces)
当前存在很多 PHP 代码，不同的库有可能包含相同的类名。命名空间解决了同一项目引入不同库而引发的命名冲突。
[PSR-4]() 是命名空间的推荐使用惯例，包括标准文件、类、命名空间，旨在让库即插即用。
2014 年 10 月，PHP-FIG 废弃了上一个自动加载标准： PSR-0，而采用新的自动加载标准 PSR-4。但 PSR-4 要求 PHP 5.3 以上的版本，而许多项目都还是使用 PHP 5.2，所以目前两者都能使用。如果你在新应用或扩展包中使用自动加载标准，应优先考虑使用 PSR-4。
- [命名空间](http://php.net/language.namespaces)
- [PSR-0](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-0.md)
- [PSR-4](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-4-autoloader.md)

### PHP 标准库 (Standard PHP Library SPL)
PHP 标准库(Standard PHP Library SPL）提供一套类和接口，包含了常用的数据结构类 (堆栈，队列，堆等等)，以及遍历这些数据结构的迭代器。或者你可以自己实现 SPL 接口。
- [SPL](http://php.net/book.spl)
- [SPL video course on Lynda.com(Paid)](http://www.lynda.com/PHP-tutorials/Up-Running-Standard-PHP-Library/175038-2.html)

### 命令行接口 (Command Line Interface CLI)
PHP 为了 Web应用而生，但它的脚本命令行也是很有用的





