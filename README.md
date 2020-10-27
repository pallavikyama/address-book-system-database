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

## UC-6-RetrievePersonsBelongingToACityOrState
### To add new contacts
```
INSERT INTO address_book(first_name,last_name,address,city,state,zip,phone_number,email) VALUES
('Srinivasulu','Kyama','Meerpet','Hyderabad','Telangana','500097','8585858787','kyamasri@gmail.com'),
('Nirmala','Kyama','Kazipet','Warangal','Telangana','506004','9494949394','nirmala@gmail.com'),
('Sritaran','Kyama','Santacruz East','Mumbai','Maharashtra','400055','6362626262','taran@gmail.com');
```

### To get data of persons belonging to a city or state
```
SELECT first_name FROM address_book WHERE city='Mumbai';
SELECT first_name FROM address_book WHERE state='Telangana';
```

## UC-7-UnderstandSizeOfAddressBookByCityOrState
### To count the number of entries in the address book using city or state
```
SELECT city,COUNT(first_name) FROM address_book GROUP BY city;
SELECT state,COUNT(first_name) FROM address_book GROUP BY state; 
```

## UC-8-RetrievePersonsAlphabeticallyForaCity
### To get entries sorted alphabetically by person's name in a particular city 
```
SELECT * FROM address_book  WHERE city='Mumbai' ORDER BY first_name;
SELECT * FROM address_book WHERE city='Hyderabad' ORDER BY first_name ;
SELECT * FROM address_book WHERE city='Warangal' ORDER BY first_name ;
```