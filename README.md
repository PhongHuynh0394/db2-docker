# Docker IBM DB2

This repo using [ibmcom/db2](https://hub.docker.com/r/ibmcom/db2/) image.

.env file:
```env
LICENSE=accept
DB2INSTANCE=db2inst1
DB2INST1_PASSWORD=rootadmin
DBNAME=testdb
BLU=false
ENABLE_ORACLE_COMPATIBILITY=false
UPDATEAVAIL=NO
TO_CREATE_SAMPLEDB=false
REPODB=false
IS_OSXFS=false
PERSISTENT_HOME=false
HADR_ENABLED=false
ETCD_ENDPOINT=
ETCD_USERNAME=
ETCD_PASSWORD=
```

To run: `docker compose up -d`

To check log: `docker logs db2`

To using db2 commandline processor (CLP):
```bash
docker exec -it db2 bash
su - db2inst1 # base on your db2 instance config in .env
db2
```
