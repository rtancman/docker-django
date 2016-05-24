FROM python:3.5-slim

RUN apt-get update
RUN apt-get install -y supervisor \
        mysql-client \
        gcc \
        gettext \
        mysql-client libmysqlclient-dev \
        postgresql-client libpq-dev \
        sqlite3 \
        python-dev \
        python-setuptools \
        libtiff5-dev zlib1g-dev \
        libfreetype6-dev liblcms2-dev libwebp-dev tcl8.6-dev tk8.6-dev python-tk

RUN touch /usr/local/bin/docker-entrypoint
RUN chmod +x /usr/local/bin/docker-entrypoint

RUN pip install --upgrade pip

WORKDIR /var/www/html

ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]