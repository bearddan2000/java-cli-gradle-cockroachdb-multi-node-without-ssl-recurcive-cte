# java-cli-gradle-cockroachdb-multi-node-without-ssl-recurcive-cte

## Description
Creates a small database table
called `dog`. This table, `dog`, has been normalized to 3NF.
Two new tables have been added, `breedLookup` and `colorLookup`.
Creates a new table `dog_expanded` that joins
`dog`, `breedLookup` and `colorLookup`.

Turned `dog_expanded` into a view with an
implicit index on `dog_expanded`.id. Using the aggregate function
COUNT, create a new view `breed_count` using recurcive common table expression.

All output normally
seen in a terminal will be in `log` which will dump to the screen. The project may seem to hang but the logs from the container must be written to the project this can take up to 3 min.

A java gradle build, that connects to 3 node cluster
cockroach database without ssl.

## Tech stack
- java
- gradle
  - postgres drivers

## Docker stack
- cockroachdb/cockroach:v19.2.2
- gradle:jdk11

## To run
`sudo ./install.sh -u`
- [Master node webui](http://localhost:8000)
- [Slave node 1 webui](http://localhost:8001)
- [Slave node 2 webui](http://localhost:8002)

## To stop
`sudo ./install.sh -d`

## For help
`sudo ./install.sh -h`

## Credit
[Cockroach setup](https://github.com/s0rg/cockroach-compose)
