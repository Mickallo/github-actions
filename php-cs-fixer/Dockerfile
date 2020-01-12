FROM php:cli-alpine

LABEL "com.github.actions.name"="PHP CS FIXER"
LABEL "com.github.actions.description"="Lint php files against coding standards"
LABEL "com.github.actions.icon"="check"
LABEL "com.github.actions.color"="blue"

LABEL "repository"="http://github.com/Mickallo/actions/php-cs-fixer"
LABEL "homepage"="http://github.com/Mickallo/actions"
LABEL "maintainer"="mickallo <mickallo@gmail.com>"

RUN wget https://github.com/FriendsOfPHP/PHP-CS-Fixer/releases/download/v2.16.1/php-cs-fixer.phar -O php-cs-fixer \
    && chmod a+x php-cs-fixer \
    && mv php-cs-fixer /usr/local/bin/php-cs-fixer

ENTRYPOINT ["php-cs-fixer", "fix", "--dry-run", "--diff"]