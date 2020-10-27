# AddressBook-Service-Database

## UC-1-CreateAddressbookServiceDatabase
### To create database
```
CREATE DATABASE addressbook_service;
SHOW DATABASES;
```

## UC-2-CreateAddressBookTableWithAttributes
### To change database
```
USE addressbook_service;
```

### To create table with first_name,last_name,address,city,state,zip,phone_number,email as fields
```
CREATE TABLE address_book
(
first_name   VARCHAR(30) NOT NULL,
last_name    VARCHAR(30),
address      VARCHAR(150) NOT NULL,
city         VARCHAR(30) NOT NULL,
state        VARCHAR(30) NOT NULL,
zip          VARCHAR(7) NOT NULL,
phone_number VARCHAR(15),
email        VARCHAR(30)
);
```

### To get table structure
```
DESCRIBE address_book;
```