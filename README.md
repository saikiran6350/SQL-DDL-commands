# SQL-DDL-commands
Microsoft Windows [Version 10.0.19045.3208]
(c) Microsoft Corporation. All rights reserved.

C:\Users\SAIKIRAN>cd/

C:\>cd xampp

C:\xampp>cd mysql

C:\xampp\mysql>cd bin

C:\xampp\mysql\bin>mysql.exe -u root
Welcome to the MariaDB monitor.  Commands end with ; or \g.
Your MariaDB connection id is 10
Server version: 10.4.24-MariaDB mariadb.org binary distribution

Copyright (c) 2000, 2018, Oracle, MariaDB Corporation Ab and others.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

MariaDB [(none)]> create database info;
Query OK, 1 row affected (0.003 sec)

MariaDB [(none)]> use info;
Database changed
MariaDB [info]> create table studentdetails(name varchar(100),id int(10),address varchar(100),phno int(10));
Query OK, 0 rows affected (0.042 sec)

MariaDB [info]> desc studentdetails;
+---------+--------------+------+-----+---------+-------+
| Field   | Type         | Null | Key | Default | Extra |
+---------+--------------+------+-----+---------+-------+
| name    | varchar(100) | YES  |     | NULL    |       |
| id      | int(10)      | YES  |     | NULL    |       |
| address | varchar(100) | YES  |     | NULL    |       |
| phno    | int(10)      | YES  |     | NULL    |       |
+---------+--------------+------+-----+---------+-------+
4 rows in set (0.020 sec)

MariaDB [info]> alter table studentdetails add deparment varchar(10);
Query OK, 0 rows affected (0.022 sec)
Records: 0  Duplicates: 0  Warnings: 0

MariaDB [info]> desc studentdetails;
+-----------+--------------+------+-----+---------+-------+
| Field     | Type         | Null | Key | Default | Extra |
+-----------+--------------+------+-----+---------+-------+
| name      | varchar(100) | YES  |     | NULL    |       |
| id        | int(10)      | YES  |     | NULL    |       |
| address   | varchar(100) | YES  |     | NULL    |       |
| phno      | int(10)      | YES  |     | NULL    |       |
| deparment | varchar(10)  | YES  |     | NULL    |       |
+-----------+--------------+------+-----+---------+-------+
5 rows in set (0.023 sec)

MariaDB [info]> alter table studentdetails drop address;
Query OK, 0 rows affected (0.031 sec)
Records: 0  Duplicates: 0  Warnings: 0

MariaDB [info]> desc studentdetails;
+-----------+--------------+------+-----+---------+-------+
| Field     | Type         | Null | Key | Default | Extra |
+-----------+--------------+------+-----+---------+-------+
| name      | varchar(100) | YES  |     | NULL    |       |
| id        | int(10)      | YES  |     | NULL    |       |
| phno      | int(10)      | YES  |     | NULL    |       |
| deparment | varchar(10)  | YES  |     | NULL    |       |
+-----------+--------------+------+-----+---------+-------+
4 rows in set (0.033 sec)

MariaDB [info]> alter table studentdetails change id rollno int(10);
Query OK, 0 rows affected (0.019 sec)
Records: 0  Duplicates: 0  Warnings: 0

MariaDB [info]> desc studentdetails;
+-----------+--------------+------+-----+---------+-------+
| Field     | Type         | Null | Key | Default | Extra |
+-----------+--------------+------+-----+---------+-------+
| name      | varchar(100) | YES  |     | NULL    |       |
| rollno    | int(10)      | YES  |     | NULL    |       |
| phno      | int(10)      | YES  |     | NULL    |       |
| deparment | varchar(10)  | YES  |     | NULL    |       |
+-----------+--------------+------+-----+---------+-------+
4 rows in set (0.016 sec)

MariaDB [info]> alter table studentdetails modify name varchar
    -> alter table studentdetails modify name varchar(100;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MariaDB server version for the right syntax to use near 'alter table studentdetails modify name varchar(100' at line 2
MariaDB [info]> alter table studentdetails modify name varchar(10);
Query OK, 0 rows affected (0.081 sec)
Records: 0  Duplicates: 0  Warnings: 0

MariaDB [info]> desc studentdetails;
+-----------+-------------+------+-----+---------+-------+
| Field     | Type        | Null | Key | Default | Extra |
+-----------+-------------+------+-----+---------+-------+
| name      | varchar(10) | YES  |     | NULL    |       |
| rollno    | int(10)     | YES  |     | NULL    |       |
| phno      | int(10)     | YES  |     | NULL    |       |
| deparment | varchar(10) | YES  |     | NULL    |       |
+-----------+-------------+------+-----+---------+-------+
4 rows in set (0.021 sec)

MariaDB [info]>





