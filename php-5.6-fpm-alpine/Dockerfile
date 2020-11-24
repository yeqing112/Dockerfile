FROM alpine:3.8

RUN sed -i 's~dl-cdn.alpinelinux.org~mirrors.aliyun.com~' /etc/apk/repositories \
    && apk --update --no-cache add php5 php5-pgsql php5-zip php5-cgi php5-embed php5-xmlrpc php5-sysvshm php5-mysql php5-imap php5-doc php5-common php5-calendar php5-pdo_dblib php5-mysqli php5-odbc php5-soap php5-shmop php5-wddx php5-cli php5-suhosin php5-fpm php5-phpdbg php5-bz2 php5-sockets php5-pdo_mysql php5-sysvmsg php5-pspell php5-iconv php5-dev php5-ftp php5-gettext php5-mssql php5-mcrypt php5-exif php5-xmlreader php5-gd php5-xml php5-pcntl php5-pear php5-pdo_pgsql php5-phar php5-apcu php5-ctype php5-intl php5-pdo php5-openssl php5-sysvsem php5-posix php5-pdo_sqlite php5-dom php5-curl php5-xsl php5-ldap php5-pdo_odbc php5-json php5-enchant php5-bcmath php5-opcache php5-sqlite3 php5-gmp php5-zlib \
    && rm -rf /var/cache/apk/*
	
COPY php.ini /etc/php5/conf.d/50-setting.ini
COPY php-fpm.conf /etc/php5/php-fpm.conf

EXPOSE 9000

CMD ["php-fpm5", "-F"]
