FROM alpine:3.7

RUN sed -i 's~dl-cdn.alpinelinux.org~mirrors.aliyun.com~' /etc/apk/repositories \
	&& apk --update --no-cache add php7 php7-fpm php7-bcmath php7-bz2 php7-calendar php7-curl php7-dba php7-enchant php7-exif php7-ftp php7-gd php7-gettext php7-gmp php7-imap php7-intl php7-ldap php7-mbstring php7-mysqli php7-pcntl php7-pdo_mysql php7-pdo_odbc php7-pdo_pgsql php7-pgsql php7-pspell php7-recode php7-shmop php7-soap php7-sockets php7-tidy php7-wddx php7-xmlrpc php7-xsl php7-zip php7-imagick php7-mcrypt php7-memcached php7-oauth php7-ssh2 php7-pdo_dblib php7-redis php7-opcache php7-openssl php7-mysqlnd php7-dom php7-ctype php7-iconv php7-json php7-pdo_sqlite php7-pdo php7-phar php7-posix php7-xml php7-zlib php7-session php7-fileinfo php7-simplexml php7-sqlite3 php7-tokenizer php7-xmlreader php7-xmlwriter \
        && rm -rf /var/cache/apk/*
	
COPY php.ini /etc/php7/conf.d/50-setting.ini
COPY php-fpm.conf /etc/php7/php-fpm.conf

EXPOSE 9000

CMD ["php-fpm7", "-F"]
