## EXPERIMENT 06:SET OPERATIONS
## AIM:
The aim of this program is to perform set operations (Union, Union All, Intersect, and Except) between two tables, A and B, in order to combine, find common elements, or identify differences between the tables.

## ALGORITHM:
1. Create table A with attributes ID and name.
2. Create table B with attributes ID and name.
3. Insert values into table A.
4. Insert values into table B.
5. Display the contents of table A.
6. Display the contents of table B.
7. Perform set operations:
a. Union: Combine rows from table A and table B, eliminating duplicates.
b. Union All: Combine rows from table A and table B, including duplicates.
c. Intersect: Find common rows between table A and table B.
d. Except: Find rows in table A that do not exist in table B.
8. Display the results of each set operation.

## PROGRAM:
```
create database if not exists MyDatabase;
use MyDatabase;
CREATE TABLE A (
  ID INTEGER PRIMARY KEY,
  name TEXT
);

CREATE TABLE B (
  ID INTEGER PRIMARY KEY,
  name TEXT
);

-- Insert values into table A
INSERT INTO A VALUES (1, 'John');
INSERT INTO A VALUES (2, 'Alice');
INSERT INTO A VALUES (3, 'Bob');

-- Insert values into table B
INSERT INTO B VALUES (2, 'Alice');
INSERT INTO B VALUES (3, 'Bob');
INSERT INTO B VALUES (4, 'Charlie');

-- Display table A
SELECT * FROM A;

-- Display table B
SELECT * FROM B;

SELECT * FROM A
UNION
SELECT * FROM B;

SELECT * FROM A
UNION ALL
SELECT * FROM B;

SELECT * FROM A
INSERTSET;
SELECT * FROM B;

SELECT * FROM A
EXCEPT
SELECT * FROM B;
```
## OUTPUT:
### The output for table A will be:
![image](https://github.com/Evangelin-Ruth/dbms-ex6/assets/94219798/0e671708-273f-4424-b165-7a66ddee439c)
### The output for table B will be:
### Union:
![image](https://github.com/Evangelin-Ruth/dbms-ex6/assets/94219798/ad5bfae7-70fb-4569-9384-af932a0ff89a)
### Union All:
![image](https://github.com/Evangelin-Ruth/dbms-ex6/assets/94219798/f60f888d-7bed-40a8-83d6-458ec051e2f0)
### Intersect:
![image](https://github.com/Evangelin-Ruth/dbms-ex6/assets/94219798/278077e0-eee7-4203-8555-63da5233778f)
### Except:
![image](https://github.com/Evangelin-Ruth/dbms-ex6/assets/94219798/2132880a-e84a-4844-abf6-333972578dd4)
## RESULT:
These results illustrate the outcomes of the set operations performed on tables A and B.


