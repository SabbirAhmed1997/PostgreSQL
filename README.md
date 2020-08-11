# PostgreSQL
This repository was opened as a part of my work with Brilliant.org.

### What you'll learn?
    In this tutorial you'll learn about database, database management system(DBMS),
    query language(SQL) and postgresql.

### What is database?
    A database is an ordered collection of data that can be easily stored, managed
    and retrieved.

### What is database management system(DBMS)?
    A Database Management System (DBMS) is a software designed to store, retrieve,
    define and manage data in a database.


### What are the types of database management system?
    Four types of DBMS are:
    * Hierarchical database
    * Network database
    * Relational database
    * Object-Oriented database

1.  Hierarchical DBMS:
    In a hierarchical database, model data is organized in a tree like structure.
    Data is stored hierarchically (top down or bottom up) format. Data is presented
    using a parent-child relationship. In hierarchical DBMS parent may have many
    children, but children have only one parent.

2.  Network DBMS:
    The network database model allows each child to have multiple parents. It helps
    to address the need to model more complex relationship like as the orders/
    parts many-to-many relationship. In this model, entities are organized in a 
    graph which can be accessed through several paths.

3.  Relational DBMS:
    Relational DBMS is the most widely used DBMS model because it is one of the 
    easiests. This model is based on normalizing data in the rows and columns of
    the tables. Relational model stored in fixed structures and manipulated using
    Structured Query Language (SQL).

4.  Object-Oriented Model:
    In Object-Oriented model data are stored in the form of objects. The structure
    is called classes which display data within it. It defines a database as a 
    collection of objects which stores both data members values and operations.


### Popular DBMS Software:
    * MySQL
    * Microsoft Access
    * Oracle
    * PostgreSQL
    * dBASE
    * FoxPro
    * SQLite
    * IBM DB2
    * LibreOffice Base
    * MariaDB
    * Microsoft SQL Server etc.

### Database Language:
    A DBMS has appropriate languages and interfaces to express database queries 
    and updates. Database languages are used to read, store and update the data in
    the database.

### Types of Database Language:
    Four types of database languages are:
    1. Data Definition Language (DDL)
    2. Data Manipulation Language (DML)
    3. Data Control Language (DCL)
    4. Transaction Control Language

### Structured Query Language (SQL):
    SQL is used to perform operations on the data stored in the database such as:
    updating records, deleting records, creating and modifying tables, views etc.
    
    _NOTE: SQL is just a query language. To perform SQL queries, you'll need to 
    install any DBMS, for example - Oracle, MySQL, PostgreSQL, MongoDB, SQL Server,
    DB2 etc._


### What is PostgreSQL?
    PostgreSQL is an advanced, powerful, open source relational database system.
    It supports both SQL (relational) and JSON (non-relational) querying. It is 
    used as a primary database for many web applications as well as mobile and 
    analytics applications.

### Languages Supported by PostgreSQL:
    It supports most of the popular programming languages:
        * Python
        * Java
        * C#
        * C/C++
        * Ruby
        * Javascript
        * Perl
        * Go

### Who uses PostgreSQL?
    Many companies have built products and solutions based on PostgreSQL. Some
    featured companies are Apple, Fujitsu, Red Hat, Cisco, Juniper Network, Istagram.


### How to install Postgresql?
1. Linux:

2. Windows:

3. Mac:

### What is pgadmin?

### How to open psql shell?
1. Linux & Mac:
   1. Open the terminal window. (Press and hold CTRL + ALT + T).
   2. In the terminal type 'sudo -i -u postgres'. It should print postgres@your_computer_name.
      (e.g. postgres@Sabbir-Lenovo-ideapad-Y700-15isk:~$)
   3. Now type psql and hit ENTER. If it prompts for password, type the password which you set during installation.
      It should display like this: postgres=#.
      NOTE: postgres is a database that is created by default.

2. Windows:

### Most important command of PSQL shell:
-  help:
   It will show some essential commands to work with. It'll also display some commands to explore more about SQL & PSQL commands
   e.g. \h and \?.

-  \l
   It'll list all the databases in your server.

-  \dt
   It'll display all the tables in your current database.


### How to create your own database?
    In the psql shell, type CREATE DATABASE database_name; In place of database_name, type a name whatever you want. Don't
    forget to insert semicolon(;) at the end of the statement. If you don't get any error, type '\l' to check whether the
    database name you provided exists or not on the list displayed. If it is there i.e. you've created your own database.

### How to connect to your database?
    In the psql shell, type '\c database_name' where '\c' means connection. Now you should see 'database_name=#' in place of
    'postgres=#'. If your database name is 'test' then you'll see 'test=#'.

### How to create table in your database?
    If you've managed to create your own database and could connect with the database then you're probably thinking how can 
    you store data in it, right? We actually store data in database using table. For this reason you have to create table in
    your database.\

    Let's say we want to create a table and we want to give the name of table as 'person' where we want to store some information
    about a person such as: first_name, last_name, email, gender, date_of_birth, country_of_birth etc. For this purpose we need to
    type the following command:\n
    ```
    CREATE TABLE person (
        id BIGSERIAL,
        first_name VARCHAR(50),
        last_name VARCHAR(50),
        email VARCHAR(150),
        gender VARCHAR(7),
        date_of_birth DATE NOT NULL,
        country_of_birth VARCHAR(50)    
    );
    ```
    I'll use this database to show you how the SQL command works throughout the whole file.
    
### Some Operations:
SELECT * FROM person;
SELECT * FROM person ORDER BY country_of_birth;
SELECT * FROM person ORDER BY country_of_birth DESC;

#### Displays information of a particular column:
     SELECT country_of_birth FROM person;
#### Keep the same countries together:
     SELECT country_of_birth FROM person ORDER By country_of_birth;
#### Display the unique countries from column country_of_birth:
     SELECT DISTINCT country_of_birth FROM person ORDER BY country_of_birth;


