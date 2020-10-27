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

## UC-3-InsertNewContactsToAddressBook
### To insert data into table
```
INSERT INTO address_book(first_name,last_name,address,city,state,zip,phone_number,email) VALUES
('Pallavi','Kyama','LBNagar','Hyderabad','Telangana','500070','8787878787','kyamap@gmail.com'),
('Padma','Gaddam','Goa','Goa','Goa','909008','9494949494','padma@gmail.com'),
('Kalpana','Kyama','JubileeHills','Hyderabad','Telangana','501009','6262626262','kalpana@gmail.com');
```

### To view all records in table
```
SELECT * FROM address_book;
```

## UC-4-EditExistingContactUsingName
### To edit existing contact person's details using their first_name
```
UPDATE address_book SET address='Borivali',city='Mumbai',state='Maharashtra',zip='400092' WHERE first_name='Kalpana';
```

### To view all records in table
```
SELECT * FROM address_book;
```

## UC-5-DeleteExistingContactUsingName
### To delete existing contact person's details using their first_name
```
DELETE FROM address_book WHERE first_name='Padma';
```

### To view all records in table
```
SELECT * FROM address_book;
```