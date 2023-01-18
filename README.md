# Neo4j Backup Restore Database Version 5


## Backup Offline Database
#### Step 1
Syntax:

    stop database arlidev WAIT;
    
#### Step 2
Syntax:

    ./neo4j-admin database dump arlidev --to-path=/home/ddi/neo4j-enterprise-5.3.0/backups

#### output: 
    /home/ddi/neo4j-enterprise-5.3.0/backups/arlidev.dump

## Restore database.dump
#### Step 1
Syntax:

    ./neo4j-admin database load --from-path=/home/ddi/neo4j-enterprise-5.3.0/backups arlidev --overwrite-destination

#### Step 2
create database arlidev in neo4j browser

Syntax:

    create database arlidev

## Backup Online Database 
Syntax:

    ./neo4j-admin database backup --to-path=/home/ddi/neo4j-enterprise-5.3.0/backups sosmed

## Restore Online Database 
Syntax:

    ./neo4j-admin database restore --from-path=/home/ddi/neo4j-enterprise-5.3.0/backups/sosmed-2023-01-18T04-12-17.backup --overwrite-destination sosmed2



