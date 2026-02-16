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

Oracle database: Oracle21c

Tools: Sql developer and sql plus

OEM Link: https://localhost:5500/em

--

## Creating the main pluggable database

Task 1: PDB CREATION COMMAND
--

1. Connecting as sys with SYSBDA role

2. PDB creation

       CREATE PLUGGABLE DATABASE Em_PDB_29068
       ADMIN USER pdbadmin IDENTIFIED BY 123
       FILE_NAME_CONVERT = ('pdbseed','Em_PDB_29068');

<img width="486" height="207" alt="CREATING PDB" src="https://github.com/user-attachments/assets/2e6ee315-01af-4fc9-84d6-e44a67dcbdcc" />

3. Opened pdb

       ALTER PLUGGABLE DATABASE Em_PDB_29068 OPEN;
 
<img width="527" height="160" alt="ALTER TO OPEN" src="https://github.com/user-attachments/assets/cc04c3f6-1ee8-4933-ab61-2fc35562b202" />

4. Switched to the PDB

       ALTER SESSION SET CONTAINER = Em_PDB_29068;

<img width="427" height="134" alt="Switch to PDB" src="https://github.com/user-attachments/assets/22c0ddcb-3f1d-44b1-8640-368617e0d3f2" />

Created User and granted all privileges

    CREATE USER Emerine_plsqlauca_29068 IDENTIFIED BY 123;
    GRANT CONNECT, RESOURCE TO Emerine_plsqlauca_29068;

<img width="553" height="202" alt="Created the user and granted " src="https://github.com/user-attachments/assets/7e8edef2-a393-4fd2-be4c-2880c38acefc" />

Task 2: Creating a temporary PDB and deletion
--

1. Create PBD and closing PDB for deletion

       CREATE PLUGGABLE DATABASE Em_TO_DELETE_PDB_29068
       ADMIN USER pdbadmin IDENTIFIED BY 1234
       FILE_NAME_CONVERT = ('pdbseed','Em_TO_DELETE_PDB_29068');
       ALTER PLUGGABLE DATABASE Em_TO_DELETE_PDB_29068 CLOSE IMMEDIATE;

<img width="570" height="202" alt="ALTER TO SAVE" src="https://github.com/user-attachments/assets/b6baa842-91fb-4a15-912e-51c31b732313" />

2.Deleting PDB and Checking

    DROP PLUGGABLE DATABASE Em_TO_DELETE_PDB_29068 INCLUDING DATAFILES;
    SHOW PDBS;
    
<img width="643" height="216" alt="DROPPING AND CHECKING" src="https://github.com/user-attachments/assets/f82e8f4f-2917-485f-9d6a-8bf5e0e48047" />





   
