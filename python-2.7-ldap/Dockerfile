FROM rtancman/django:2.7

RUN apt-get update && apt-get install -y libldap2-dev \
    libsasl2-dev libssl-dev \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /var/www/html

ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]