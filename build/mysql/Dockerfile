FROM mysql:5.7

ARG LOCAL_USER_ID=1000
ARG LOCAL_GROUP_ID=1000

RUN set -ex \
  && usermod -u $LOCAL_USER_ID mysql \
  && groupmod -g $LOCAL_GROUP_ID mysql

VOLUME ["/var/lib/mysql"]

EXPOSE 3306
