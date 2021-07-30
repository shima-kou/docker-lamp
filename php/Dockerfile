FROM php:apache
RUN apt-get update -y

# PHPのExtensionをインストール
# 最新のphp:apachコンテナでは, mbstringインストールにorigurumaがないことでエラー発生
# => 代わりにlibonig-devを入れる
# 参考：https://qiita.com/June8715/items/1df5958b95c1ff2d4c1b
RUN apt-get install libonig-dev -y
RUN docker-php-ext-install pdo_mysql

WORKDIR /var/www/html

EXPOSE 80