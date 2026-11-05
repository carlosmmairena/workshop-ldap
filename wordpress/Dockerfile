FROM wordpress:php8.3-apache

# Instala la librería de desarrollo de LDAP y compila la extensión PHP
RUN apt-get update \
 && apt-get install -y --no-install-recommends libldap2-dev \
 && docker-php-ext-configure ldap --with-libdir=lib/$(uname -m)-linux-gnu/ \
 && docker-php-ext-install ldap \
 && rm -rf /var/lib/apt/lists/*
