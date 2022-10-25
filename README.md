# MariaREDME

//Database creation command and output
MariaDB [(none)]> CREATE DATABASE ndjulu;
Query OK, 1 row affected (0.004 sec)


//Checking the list of available databases and output

MariaDB [(none)]> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| ndjulu             |
| performance_schema |
| test               |
+--------------------+
5 rows in set (0.002 sec)

//User creation and results

MariaDB [(none)]> use ndjulu;
Database changed
MariaDB [ndjulu]> create user 'user_[ndjulu]'@localhost IDENTIFIED BY 'Naledi97';
Query OK, 0 rows affected (0.081 sec)

// Selecting the User

MariaDB [ndjulu]> Select user FROM mysql.user;
+---------------+
| User          |
+---------------+
| root          |
| root          |
| root          |
| root          |
| mariadb.sys   |
| root          |
| user_[ndjulu] |
+---------------+
7 rows in set (0.115 sec)

// Granting user privileges to read data on the database from anywhere

MariaDB [ndjulu]> GRANT ALL PRIVILEGES ON  *.* TO 'user_[ndjulu]'@localhost IDENTIFIED BY 'Naledi97';
Query OK, 0 rows affected (0.062 sec)

MariaDB [ndjulu]> GRANT ALL PRIVILEGES ON ndjulu.* TO 'user_[ndjulu]'@localhost;
Query OK, 0 rows affected (0.088 sec)

TASK 2
//This code 
<?php

echo "This is Ndjulu";

//This code 

<VirtualHost *80>

DocumentRoot "C:\websites\ndjulu"
ServerName ndjulu.local

<Directory "C:\websites\ndjulu"
     Options Indexes FollowSymLinks Includes ExecCGI
     AllowOverride All
     Require all granted
</Directory>
</VirtualHost>

//This code

#localhost name resolution is handled within DNS itself.
#	127.0.0.1 localhost
#	::1 localhost
    
    127.0.0.1 localhost
    ::1 localhost
    127.0.0.1 ndjulu.local
    <?php

//This code connects the database to phpMyAdmin

$dbServername = "localhost";
$dbUsername ="root";
$dbPassword = "Naledi97"
$dbName = "ndjulu";

$conn = mysqli_connect($dbServername, $dbUsername, $dbPassword, $dbName)
