
Example stack.yml for owncloud:

# ownCloud with MariaDB/MySQL
#
# Access via "http://localhost:8080" (or "http://$(docker-machine ip):8080" if using docker-machine)
#
# During initial ownCloud setup, select "Storage & database" --> "Configure the database" --> "MySQL/MariaDB"
# Database user: root
# Database password: example
# Database name: pick any name
# Database host: replace "localhost" with "mysql"

version: '3.1'

services:

  owncloud:
    image: owncloud
    restart: always
    ports:
      - 8080:80

  mysql:
    image: mariadb
    restart: always
    environment:
      MYSQL_ROOT_PASSWORD: example
      





