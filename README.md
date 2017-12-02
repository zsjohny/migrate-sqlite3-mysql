# migrate-sqlite3-mysql
Migrating Bolt CMS from SQLite to MySQ


## Export and convert SQLite database to MySQL dump
cd app/database/
sqlite3 bolt.db .dump | ./sqlite3-to-mysql.py > bolt.sql

## Import MySQL dump to your server
Execute:

mysql -ubolt -pSOMEPASSWORD bolt
source bolt.sql
