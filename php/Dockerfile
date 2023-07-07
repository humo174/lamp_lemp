FROM php:8.1-fpm

RUN apt-get update && apt-get install -y \
		libfreetype-dev \
		libjpeg62-turbo-dev \
		libpng-dev \	
	&& docker-php-ext-configure gd --with-freetype --with-jpeg \
	&& docker-php-ext-install -j$(nproc) gd \
	&& docker-php-ext-install -j$(nproc) mysqli \
	&& docker-php-ext-install -j$(nproc) opcache
	
RUN apt-get update && apt-get install -y zlib1g-dev libzip-dev sendmail

RUN docker-php-ext-install pdo_mysql
RUN docker-php-ext-install zip

RUN sed -i '/#!\/bin\/sh/aservice sendmail restart' /usr/local/bin/docker-php-entrypoint
RUN sed -i '/#!\/bin\/sh/aecho "$(hostname -i)\t$(hostname) $(hostname).localhost" >> /etc/hosts' /usr/local/bin/docker-php-entrypoint	

COPY cfg/conf.d /usr/local/etc/php/
COPY cfg/php.ini /usr/local/etc/php/
