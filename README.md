Run postgres and pgadmin together in docker.

# Setup

Create a file named `.env` in this directory for docker environment variables.  This file contain variables in the following format:
```
VARIABLE_NAME=value1
VARIABLE_TWO=value2
```

Set the following variables in the `.env` files:

   * **PGADMIN_EMAIL** - email address you'll use to log in to pgAdmin
   * **PGADMIN_PASSWORD** - password you'll use to login to pgAdmin
   * **PGADMIN_PORT** - port used to access pgAdmin (optional, defaults to 2345)
   * **POSTGRES_VERSION** - version of PostgreSQL to run (optional, defaults to 'latest')
   * **POSTGRES_USER** - default Postgres user name
   * **POSTGRES_PASSWORD** - password for the default Postgres user
   * **POSTGRES_PORT** - port used to access the Postgres instance (optional, defaults to 5432)

After saving changes to the `.env` file, run `docker-compose up -d` to start the containers.  You can access pgAdmin in the browser at http://localhost:2345 (or whatever port you specified).  Note that when you add the Postgres database to pgAdmin, you'll need to specify the database host name as "postgres".