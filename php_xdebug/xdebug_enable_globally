#!/bin/bash
cat /usr/local/etc/php/conf.d/xdebug.ini.en | \
        sudo tee \
        /etc/php/7.0/mods-available/xdebug.ini \
        /etc/php/7.1/mods-available/xdebug.ini  \
        /etc/php/7.2/mods-available/xdebug.ini  \
        /etc/php/7.3/mods-available/xdebug.ini \
        /etc/php/7.4/mods-available/xdebug.ini \
        > /dev/null
cat /usr/local/etc/php/conf.d/xdebug-56.ini.en | \
        sudo tee /etc/php/5.6/mods-available/xdebug.ini \
        > /dev/null
