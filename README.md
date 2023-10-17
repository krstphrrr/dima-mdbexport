## script to extract tables from MSAccess databases

### Requirements

- Local installation of Docker (docker desktop 4.24+ if on Windows)

### description
Leverages mdbtools and bash to batch-export selected tables from mdb files to CSV.

1. clone repository
2. deposit mdb files inside `/client-bind/mdbs`
3. run the custom script container with `docker compose up`


The script will deposit the csv files of each table inside a directory with the name of the mdb file.

## todo 
- [ ] create custom docker image with the: mdbtools, python and pgclient (to soon include the rest of the ingest script)
- [ ] create entrypoint script for the container that switches between extract and ingest (else use lighter image, not postgis)
- [ ] create transform script with straightforward transform functions(airflow ready)