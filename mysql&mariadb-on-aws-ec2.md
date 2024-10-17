# Commands used to host MySql Server on AWS EC2 Instance

## Step 1: Update the system

sudo apt update

## Step 2: Install MySql

sudo apt install mysql-server

## Step 3: Check the Status of MySql (Active or Inactive)

sudo systemctl status mysql

## Step 4: Login to MySql as a root

sudo mysql

## Step 5: Update the password for the MySql Server

ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'place-your-password-here';

FLUSH PRIVILEGES;

## Step 6: Test the MySql server if it is working by running sample sql queries

CREATE DATABASE mysql_test;

USE mysql_test;

CREATE TABLE table1 (id INT, name VARCHAR(45));

INSERT INTO table1 VALUES(1, 'Virat'), (2, 'Sachin'), (3, 'Dhoni'), (4, 'ABD');

SELECT * FROM table1;




# Commands used to host mariadb-server Server on AWS EC2 Instance

sudo su -

## Step 1: Update the system

sudo apt update

## Step 2: Install mariadb-server

yum -y install mariadb-server

## Step 3: Enable of mariadb

systemctl enable mariadb

## Step 4: Start of mariadb

systemctl start mariadb

## Step 4: Login to mariadb as a root

mysql -h {paste-rds-endpoint-here} -P 3306 -u rdsuser -p



