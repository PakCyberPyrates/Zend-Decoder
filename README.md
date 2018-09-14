# Zend-Decoder
支持php5.6 zend解密，其他版本未测。

## 编译 xcache
### Ubuntu + php5.6：
```
sudo apt-get install python-software-properties
sudo add-apt-repository ppa:ondrej/php
sudo apt-get update
apt-get install php5.6-dev
git clone https://github.com/lighttpd/xcache
cd xcache
patch -p1 < ../xcache.patch
phpize
./configure --enable-xcache-disassembler
make
make install
cp xcache.ini 
php -v
```
[编译参考](https://github.com/lighttpd/xcache/blob/master/INSTALL)

### windows + php5.6
[如何编译](https://github.com/hylent/docs/blob/master/build-php-extension-on-windows.md)
## 使用
### 修改php.ini
```
extension=xcache.so
zend_extension = ZendGuardLoader.so
或
extension=xcache.dll
zend_extension = ZendGuardLoader.dll
```
### 解码
```
php index.php encode.php
或
php index2.php encode.php

```


## Decompiler.class.php
[Decompiler.class.php](https://github.com/lighttpd/xcache/blob/master/lib/Decompiler.class.php)

