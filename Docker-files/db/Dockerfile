FROM mysql:8.0.33
LABEL "project"="vprofile"
LABEL "Author"="Imran"

# Correct the environment variable for the MySQL root password
ENV MYSQL_ROOT_PASSWORD="vprodpass"
ENV MYSQL_DATABASE="accounts"

# Add the SQL file to initialize the database
ADD db_backup.sql /docker-entrypoint-initdb.d/db_backup.sql
