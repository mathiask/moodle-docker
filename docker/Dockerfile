FROM moodlehq/moodle-php-apache:7.2

RUN pecl install xdebug-2.9.5 && docker-php-ext-enable xdebug
RUN echo 'zend_extension="/usr/local/lib/php/extensions/no-debug-non-zts-20190902/xdebug.so"' >> /usr/local/etc/php/php.ini &&\
    echo 'xdebug.remote_host=10.0.2.15' >> /usr/local/etc/php/php.ini &&\
    echo 'xdebug.remote_port=9000' >> /usr/local/etc/php/php.ini &&\
    echo 'xdebug.remote_enable=1' >> /usr/local/etc/php/php.ini &&\
    echo 'xdebug.remote_handler=dbgp' >> /usr/local/etc/php/php.ini &&\
    echo 'xdebug.idekey=docker' >> /usr/local/etc/php/php.ini &&\
    echo 'xdebug.remote_autostart=on' >> /usr/local/etc/php/php.ini
