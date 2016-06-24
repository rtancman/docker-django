FROM python:3.5-slim

RUN apt-get update && apt-get install -y supervisor \
    gcc gettext sqlite3 \
    python-dev python-setuptools \
    libtiff5-dev zlib1g-dev \
    mysql-client libmysqlclient-dev \
    postgresql-client libpq-dev \
    libfreetype6-dev liblcms2-dev libwebp-dev \
    tcl8.6-dev tk8.6-dev python-tk \
    && rm -rf /var/lib/apt/lists/*

RUN touch /usr/local/bin/docker-entrypoint && \
    chmod +x /usr/local/bin/docker-entrypoint

RUN pip install --upgrade pip \
    && apt-get purge -y --auto-remove $buildDeps \
    && rm -rf /usr/src/python ~/.cache

WORKDIR /var/www/html

ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]