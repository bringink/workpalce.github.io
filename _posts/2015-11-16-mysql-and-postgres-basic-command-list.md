### MySQL VS PostgreSQL command
|   |MySQL   | PostgreSQL |
| ------------ | ------------ | ------------ |
| access DB  | mysql  | psql  |
|access to DB as ${USER_NAME} |mysql -u ${USER_NAME} -p ${PASSWORD} -P${PORT_NUMBER} -h ${DB_SERVER} ${DB_NAME} |psql -U ${USER_NAME} -p ${PORT_NUMBER} -h ${DB_SERVER} ${DB_NAME} |
| add a new user  | grant all privileges on ${DB_NAME}.${TABLE_NAME} to '${USER_NAME}'@'${HOSTNAME}' identified by '${PASSWORD}';  |  create user ${USER_NAME}  with password ${PASSWORD} |
| check DB List  | mysql$ show databases;   | postgres=# \l   |
|create new db   | mysql$ create database ${DB_NAME};   | postgres=# create database ${DB_NAME} |
| create table  |mysql$ Create table employee(employee_id int primary key, name char(8), sex char(2));    | postgres=# create table employee(employee_id int primary key, name char(8), sex char(2));   |
|show table list from outside  |user% echo "show tables;" | mysql   | user% echo "\d" | psql ${DB_NAME} |