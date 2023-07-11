# SQL: Beginner to Advance

[Educative.io SQL: From Beginner to Advance](https://www.educative.io/module/JZmo10C1K3V0gqV0w/10370001/5844917766586368)

## Exploring

```SQL
SHOW DATABASES;
USE mysql;
SHOW CREATE DATABASE mysql;
SHOW TABLES;
DESCRIBE user;
SHOW CREATE TABLE servers;
SHOW COLUMNS FROM servers;
```

## Create Databases

```SQL
CREATE DATABASE MovieIndustry;
CREATE DATABASE IF NOT EXISTS MovieIndustry;
SHOW DATABASES;
DROP DATABASE MovieIndustry;
```

## Create Table

```SQL
CREATE TABLE IF NOT EXISTS Actors (
Id INT AUTO_INCREMENT,
FirstName VARCHAR(20) NOT NULL,
SecondName VARCHAR(20) NOT NULL,
DoB DATE NOT NULL,
Gender ENUM('Male','Female','Other') NOT NULL,
MaritalStatus ENUM('Married', 'Divorced', 'Single', 'Unknown') DEFAULT "Unknown",
NetWorthInMillions DECIMAL NOT NULL,
PRIMARY KEY (Id));

SHOW TABLES;
DESC Actors;
```

## Temporary Tables

```SQL
CREATE TEMPORARY TABLE ActorNames (FirstName CHAR(20));
```

## Insert Data

```sql
INSERT INTO Actors (
FirstName, SecondName, DoB, Gender, MaritalStatus, NetworthInMillions)
VALUES ("Brad", "Pitt", "1963-12-18", "Male", "Single", 240.00);

INSERT INTO Actors (
FirstName, SecondName, DoB, Gender, MaritalStatus, NetworthInMillions)
VALUES
("Jennifer", "Aniston", "1969-11-02", "Female", "Single", 240.00),
("Angelina", "Jolie", "1975-06-04", "Female", "Single", 100.00),
("Johnny", "Depp", "1963-06-09", "Male", "Single", 200.00);

INSERT INTO Actors
VALUES (DEFAULT, "Dream", "Actress", "9999-01-01", "Female", "Single", 000.00);

INSERT INTO Actors VALUES (NULL, "Reclusive", "Actor", "1980-01-01", "Male", "Single", DEFAULT);

INSERT INTO Actors () VALUES ();

INSERT INTO Actors SET DoB="1950-12-12", FirstName="Rajnikanth", SecondName="",  Gender="Male", NetWorthInMillions=50,  MaritalStatus="Married";
```
