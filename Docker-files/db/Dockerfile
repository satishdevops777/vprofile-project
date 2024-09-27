FROM mysql:8.0.33
LABEL "proect"="vprofile"
LABEL "Author"="Satish"
ENV MYSQL_ROOT_PASSOWORD="vprodbpass"
ENV MYSQL_DATABASE="accounts"

ADD db_backup.sql /docker-entrypoint-initdb.d/db_backup.sql
