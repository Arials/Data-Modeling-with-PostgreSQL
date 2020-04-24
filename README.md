# Sparkify

## Description

Sparkify is a new concept in the song's industry where the analysis and songs recomendations are the core.
We analyze what songs users listen to.

## How it works

To achieve that purpose, we have created a relational database in Postgre SQL to store all the information about the songs, artists and most important, songs played.

The tables are:
    
* songsplay - The most important, where the songs that the users listen to are recorded here.
* users - The users of this new service.
* songs - All the catalog of songs available.
* artists - All the artists available.
* time - The datatime where the songs was palyed.
    
## How to get the information - ETL

To get the information stored in the tables, we have needed to create an ETL process to find the correct information available in:

* Songs : Available in JSON format
* Reproductions : Available in JSON format in the log of the player.
    
We have create this ETL process using python 3.X, so we can extract the information we need from the logs and store it in the SQL tables, ready for the analysis.

## First steps

To execute the ETL process you ned to:

* Create the tables in your PostgreSQL DB:

'''
import create_tables
import etl
create_tables.main()
etl.main()
'''
