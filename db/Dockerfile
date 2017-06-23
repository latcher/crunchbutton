FROM mariadb

ADD dump.sql /docker-entrypoint-initdb.d/00000-dump.sql
ADD migrate/00048[89]* /docker-entrypoint-initdb.d/
ADD migrate/00049* /docker-entrypoint-initdb.d/

RUN (cd /docker-entrypoint-initdb.d/; sed -i.old '1s;^;use crunchbutton\;\n;' *.sql)
