# PHP xdebug fast enable/ disable
_(works with [Ondrejs multiple PHP version PPA](https://launchpad.net/~ondrej/+archive/ubuntu/php))_

## setup
* create directory `/usr/local/etc/php/conf.d/`
* pull this git
```
git pull https://github.com/Luc4G3r/linux-bash-commands.git ~/tmp
```
* move files from `~/tmp/php_xdebug` to `/usr/local/etc/php/conf.d/`
```
  mv ~/tmp/php_xdebug/*.ini.* /usr/local/etc/php/conf.d/
```
* move scripts from `~/tmp/php_xdebug` to `/usr/bin/`
```
  mv ~/tmp/php_xdebug/*.sh /usr/bin/
```
* create aliases in `~/.profile` or `~/.bash_profile`
