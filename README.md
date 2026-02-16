ORACLE PLUGGABLE DATABASE(PDB) MANAGEMENT
--

Name: UWABATO Emerine

ID: 29068

ASSIGNMENT II

--
## ASSIGNMENT OVERVIEW

This assignment was about practicing Oracle Multitenant Architecture.  

The main goal was to learn how to create and manage Pluggable Databases (PDBs), create users inside a PDB, and use Oracle Enterprise Manager (OEM) to view the database environment.

## Environment used
--

Oracle database: Oracle21c

Tools: Sql developer and sql plus

OEM Link: https://localhost:5500/em

--

## Creating the main pluggable database
--
Task 1: PDB CREATION COMMAND
--

1. Connecting as sys with SYSBDA role

2. PDB creation

       CREATE PLUGGABLE DATABASE Em_PDB_29068
       ADMIN USER pdbadmin IDENTIFIED BY 123
       FILE_NAME_CONVERT = ('pdbseed','Em_PDB_29068');



