# sql-databse
```js
Windows PowerShell
Copyright (C) Microsoft Corporation. All rights reserved.

Install the latest PowerShell for new features and improvements! https://aka.ms/PSWindows

PS C:\Users\Minfy.DESKTOP-81ME0ME> psql -U postgres
Password for user postgres:

psql: error: connection to server at "localhost" (::1), port 5432 failed: FATAL:  password authentication failed for user "postgres"
PS C:\Users\Minfy.DESKTOP-81ME0ME> psql -U postgres
Password for user postgres:

psql: error: connection to server at "localhost" (::1), port 5432 failed: FATAL:  password authentication failed for user "postgres"
PS C:\Users\Minfy.DESKTOP-81ME0ME> psql -U postgres
Password for user postgres:

psql: error: connection to server at "localhost" (::1), port 5432 failed: FATAL:  password authentication failed for user "postgres"
PS C:\Users\Minfy.DESKTOP-81ME0ME> psql -U postgres
Password for user postgres:

psql (17.5)
WARNING: Console code page (850) differs from Windows code page (1252)
         8-bit characters might not work correctly. See psql reference
         page "Notes for Windows users" for details.
Type "help" for help.

postgres=# CREATE USER kavya WITH PASSWORD 'kavya' ;
CREATE ROLE
postgres=# CREATE DATABASE university_db OWNER kavya;
CREATE DATABASE
postgres=# CREATE DATABASE university_db_2 OWNER kavya;
CREATE DATABASE
postgres=# GARANT ALL PRIVIILES ON DATABASE kavya;
ERROR:  syntax error at or near "GARANT"
LINE 1: GARANT ALL PRIVIILES ON DATABASE kavya;
        ^
postgres=# GRANT ALL PRIVIILES ON DATABASE kavya;
ERROR:  syntax error at or near "PRIVIILES"
LINE 1: GRANT ALL PRIVIILES ON DATABASE kavya;
                  ^
postgres=# GRANT ALL PRIVIILEGES ON DATABASE kavya;
ERROR:  syntax error at or near "PRIVIILEGES"
LINE 1: GRANT ALL PRIVIILEGES ON DATABASE kavya;
                  ^
postgres=# GRANT ALL PRIVILEGES ON DATABASE kavya;
ERROR:  syntax error at or near ";"
LINE 1: GRANT ALL PRIVILEGES ON DATABASE kavya;
                                              ^
postgres=# GRANT ALL PRIVILEGES ON DATABASE kavya ;
ERROR:  syntax error at or near ";"
LINE 1: GRANT ALL PRIVILEGES ON DATABASE kavya ;
                                               ^
postgres=# GRANT ALL PRIVILEGES ON DATABASE TO kavya;
ERROR:  relation "database" does not exist
postgres=# GRANT ALL PRIVILEGES ON DATABASE university_db TO kavya;
GRANT
postgres=# \q
PS C:\Users\Minfy.DESKTOP-81ME0ME> psql -U kavya -d unversity_db;
Password for user kavya:

psql: error: connection to server at "localhost" (::1), port 5432 failed: FATAL:  database "unversity_db" does not exist
PS C:\Users\Minfy.DESKTOP-81ME0ME> psql -U kavya -d unversity_db;
Password for user kavya:

psql: error: connection to server at "localhost" (::1), port 5432 failed: FATAL:  database "unversity_db" does not exist
PS C:\Users\Minfy.DESKTOP-81ME0ME> psql -U kavya -d unversity_db;
Password for user kavya:

psql: error: connection to server at "localhost" (::1), port 5432 failed: FATAL:  database "unversity_db" does not exist
PS C:\Users\Minfy.DESKTOP-81ME0ME> psql -U kavya -d unversity_db;
Password for user kavya:

psql: error: connection to server at "localhost" (::1), port 5432 failed: FATAL:  database "unversity_db" does not exist
PS C:\Users\Minfy.DESKTOP-81ME0ME> psql -U kavya -d unversity_db;
Password for user kavya:

psql: error: connection to server at "localhost" (::1), port 5432 failed: FATAL:  database "unversity_db" does not exist
PS C:\Users\Minfy.DESKTOP-81ME0ME> psql -U kavya -d university_db;
Password for user kavya:

psql (17.5)
WARNING: Console code page (850) differs from Windows code page (1252)
         8-bit characters might not work correctly. See psql reference
         page "Notes for Windows users" for details.
Type "help" for help.

university_db=> \1
invalid command \1
Try \? for help.
university_db=>  \1
invalid command \1
Try \? for help.
university_db=> \l
                                                               List of databases
      Name       |  Owner   | Encoding | Locale Provider |      Collate       |       Ctype        | Locale | ICU Rules |   Access privileges
-----------------+----------+----------+-----------------+--------------------+--------------------+--------+-----------+-----------------------
 postgres        | postgres | UTF8     | libc            | English_India.1252 | English_India.1252 |        |           |
 template0       | postgres | UTF8     | libc            | English_India.1252 | English_India.1252 |        |           | =c/postgres          +
                 |          |          |                 |                    |                    |        |           | postgres=CTc/postgres
 template1       | postgres | UTF8     | libc            | English_India.1252 | English_India.1252 |        |           | =c/postgres          +
                 |          |          |                 |                    |                    |        |           | postgres=CTc/postgres
 university_db   | kavya    | UTF8     | libc            | English_India.1252 | English_India.1252 |        |           | =Tc/kavya            +
                 |          |          |                 |                    |                    |        |           | kavya=CTc/kavya
 university_db_2 | kavya    | UTF8     | libc            | English_India.1252 | English_India.1252 |        |           |
(5 rows)


university_db=> \password
Enter new password for user "kavya":

Enter it again:

university_db=> cd ..
university_db-> cd ..
university_db->
university_db-> cd
university_db-> cd university_db
university_db-> CREATE TABLE  students(
university_db(> student_id INTEGER,
university_db(> first_name VARCHAR(50),
university_db(> email VARCHAR(100),
university_db(> date_of_birth DATE
university_db(> );
ERROR:  syntax error at or near "cd"
LINE 1: cd ..
        ^
university_db=> cd university_db
university_db-> ),
university_db-> ;
ERROR:  syntax error at or near "cd"
LINE 1: cd university_db
        ^
university_db=> CREATE TABLE  students(
university_db(> student_id INTEGER,
university_db(> first_name VARCHAR(50),
university_db(> email VARCHAR(100),
university_db(> date_of_birth DATE
university_db(> );
CREATE TABLE
university_db=> ALTER TABLE students ADD COLUMN enrollment_date DATE;
ALTER TABLE
university_db=> ALTER TABLE students DROP COLUMN enrollment_date;
ALTER TABLE
university_db=> \l
                                                               List of databases
      Name       |  Owner   | Encoding | Locale Provider |      Collate       |       Ctype        | Locale | ICU Rules |   Access privileges
-----------------+----------+----------+-----------------+--------------------+--------------------+--------+-----------+-----------------------
 postgres        | postgres | UTF8     | libc            | English_India.1252 | English_India.1252 |        |           |
 template0       | postgres | UTF8     | libc            | English_India.1252 | English_India.1252 |        |           | =c/postgres          +
                 |          |          |                 |                    |                    |        |           | postgres=CTc/postgres
 template1       | postgres | UTF8     | libc            | English_India.1252 | English_India.1252 |        |           | =c/postgres          +
                 |          |          |                 |                    |                    |        |           | postgres=CTc/postgres
 university_db   | kavya    | UTF8     | libc            | English_India.1252 | English_India.1252 |        |           | =Tc/kavya            +
                 |          |          |                 |                    |                    |        |           | kavya=CTc/kavya
 university_db_2 | kavya    | UTF8     | libc            | English_India.1252 | English_India.1252 |        |           |
(5 rows)


university_db=> select * from students
university_db-> ;
 student_id | first_name | email | date_of_birth
------------+------------+-------+---------------
(0 rows)


university_db=> ALTER TABLE students DROP COLUMN enrollment_date;
ERROR:  column "enrollment_date" of relation "students" does not exist
university_db=> ALTER TABLE students ADD COLUMN enrollment_date DATE;
ALTER TABLE
university_db=> select * from students
university_db-> ;
 student_id | first_name | email | date_of_birth | enrollment_date
------------+------------+-------+---------------+-----------------
(0 rows)


university_db=> ALTER TABLE students DROP COLUMN enrollment_date;
ALTER TABLE
university_db=> select * from students
university_db-> ;
 student_id | first_name | email | date_of_birth
------------+------------+-------+---------------
(0 rows)


university_db=> ALTER TABLE students DROP ALTER COLUMN email TYPE VARCHAR(150);
ERROR:  syntax error at or near "COLUMN"
LINE 1: ALTER TABLE students DROP ALTER COLUMN email TYPE VARCHAR(15...
                                        ^
university_db=> ALTER TABLE students ALTER COLUMN email TYPE VARCHAR(150);
ALTER TABLE
university_db=> select * from students ;
 student_id | first_name | email | date_of_birth
------------+------------+-------+---------------
(0 rows)


university_db=> ALTER TABLE students RENAME COLUMN date_of_birth TO dob;
ALTER TABLE
university_db=> select * from students ;
 student_id | first_name | email | dob
------------+------------+-------+-----
(0 rows)


university_db=> ALTER TABLE student ADD CONSTRAINT unique_email UNIQUE (email);
ERROR:  relation "student" does not exist
university_db=> ALTER TABLE students ADD CONSTRAINT unique_email UNIQUE (email);
ALTER TABLE
university_db=> select * from students ;
 student_id | first_name | email | dob
------------+------------+-------+-----
(0 rows)


university_db=> ALTER TABLE students ADD COLUMN phone_no. TYPE VARCHAR(50);
ERROR:  syntax error at or near "."
LINE 1: ALTER TABLE students ADD COLUMN phone_no. TYPE VARCHAR(50);
                                                ^
university_db=> ALTER TABLE students ADD COLUMN phone_no TYPE VARCHAR(50);
ERROR:  syntax error at or near "VARCHAR"
LINE 1: ALTER TABLE students ADD COLUMN phone_no TYPE VARCHAR(50);
                                                      ^
university_db=> ALTER TABLE students ADD COLUMN phone_no TYPE VARCHAR(50);
ERROR:  syntax error at or near "VARCHAR"
LINE 1: ALTER TABLE students ADD COLUMN phone_no TYPE VARCHAR(50);
                                                      ^
university_db=> ALTER TABLE students ADD COLUMN phone_no TYPE VARCHAR(50) ;
ERROR:  syntax error at or near "VARCHAR"
LINE 1: ALTER TABLE students ADD COLUMN phone_no TYPE VARCHAR(50) ;
                                                      ^
university_db=>  ALTER TABLE students ADD COLUMN phone_no TYPE VARCHAR(50) ;
ERROR:  syntax error at or near "VARCHAR"
LINE 1: ALTER TABLE students ADD COLUMN phone_no TYPE VARCHAR(50) ;
                                                      ^
university_db=>  ALTER TABLE students ADD COLUMN phone TYPE VARCHAR(50);
ERROR:  syntax error at or near "VARCHAR"
LINE 1: ALTER TABLE students ADD COLUMN phone TYPE VARCHAR(50);
                                                   ^
university_db=> ALTER TABLE students ALTER COLUMN phone_NO TYPE VARCHAR(150);
ERROR:  column "phone_no" of relation "students" does not exist
university_db=> ALTER TABLE students ADD COLUMN phone_NO TYPE VARCHAR(150);
ERROR:  syntax error at or near "VARCHAR"
LINE 1: ALTER TABLE students ADD COLUMN phone_NO TYPE VARCHAR(150);
                                                      ^
university_db=>  ALTER TABLE students ADD COLUMN phone_NO TYPE VARCHAR(150);
ERROR:  syntax error at or near "VARCHAR"
LINE 1: ALTER TABLE students ADD COLUMN phone_NO TYPE VARCHAR(150);
                                                      ^
university_db=>  ALTER TABLE students ADD COLUMN phone_NO TYPE INT;
ERROR:  syntax error at or near "INT"
LINE 1: ALTER TABLE students ADD COLUMN phone_NO TYPE INT;
                                                      ^
university_db=>  ALTER TABLE students ADD COLUMN phone_NO VARCHAR(150);
ALTER TABLE
university_db=>  ALTER TABLE students DROP COLUMN phone_NO VARCHAR(150);
ERROR:  syntax error at or near "VARCHAR"
LINE 1: ALTER TABLE students DROP COLUMN phone_NO VARCHAR(150);
                                                  ^
university_db=>  ALTER TABLE students DROP COLUMN phone_NO TYPE VARCHAR(150);
ERROR:  syntax error at or near "TYPE"
LINE 1: ALTER TABLE students DROP COLUMN phone_NO TYPE VARCHAR(150);
                                                  ^
university_db=>  ALTER TABLE students DROP COLUMN phone_NO VARCHAR(150);
ERROR:  syntax error at or near "VARCHAR"
LINE 1: ALTER TABLE students DROP COLUMN phone_NO VARCHAR(150);
                                                  ^
university_db=>  ALTER TABLE students DROP COLUMN phone_NO;
ALTER TABLE
university_db=> SELECT * FROM students;
 student_id | first_name | email | dob
------------+------------+-------+-----
(0 rows)


university_db=>  ALTER TABLE students ADD COLUMN last_name VARCHAR(150);
ALTER TABLE
university_db=> INSERT INTO students (student_id, first_name, last_name, email, dob)
university_db-> VALUES (1, 'Alice', 'Smith', 'alice.smith@example.com', '2003-05-15');
INSERT 0 1
university_db=> INSERT INTO students (student_id, first_name, last_name, email, dob)
university_db-> VALUES (2, 'Bob', 'Johnson', 'bob.johnson@example.com', '2002-08-22'),
university_db->        (3, 'Charlie', 'Brown', 'charlie.brown@example.com', '2003-01-10');
INSERT 0 2
university_db=> select * from students;
 student_id | first_name |           email           |    dob     | last_name
------------+------------+---------------------------+------------+-----------
          1 | Alice      | alice.smith@example.com   | 2003-05-15 | Smith
          2 | Bob        | bob.johnson@example.com   | 2002-08-22 | Johnson
          3 | Charlie    | charlie.brown@example.com | 2003-01-10 | Brown
(3 rows)


university_db=> INSERT INTO students (student_id, first_name, last_name, email, dob)
university_db-> VALUES (4, 'sanskar', 'goyal', 'sanskar@example.com', '2003-06-19');
INSERT 0 1
university_db=> INSERT INTO students (student_id, first_name, last_name, email, dob)
university_db-> VALUES (2, 'yashu', 'bharadwaj', 'yashu@example.com', '2003-04-20'),
university_db-> AJDNJA;
ERROR:  syntax error at or near "AJDNJA"
LINE 3: AJDNJA;
        ^
university_db=> INSERT INTO students (student_id, first_name, last_name, email, dob)
university_db-> VALUES (5, 'yashu', 'bharadwaj', 'yashu@example.com', '2003-04-20'),
university_db-> ;
ERROR:  syntax error at or near ";"
LINE 3: ;
        ^
university_db=> VALUES (5, 'yashu', 'bharadwaj', 'yashu@example.com', '2003-04-20'),
university_db-> D
university_db-> ;
ERROR:  syntax error at or near "D"
LINE 2: D
        ^
university_db=> INSERT INTO students (student_id, first_name, last_name, email, dob)
university_db-> VALUES (2, 'yashu', 'bharadwaj', 'yashu@example.com', '2003-04-20');
INSERT 0 1
university_db=> SELECT * FROM STUDENTS ;
 student_id | first_name |           email           |    dob     | last_name
------------+------------+---------------------------+------------+-----------
          1 | Alice      | alice.smith@example.com   | 2003-05-15 | Smith
          2 | Bob        | bob.johnson@example.com   | 2002-08-22 | Johnson
          3 | Charlie    | charlie.brown@example.com | 2003-01-10 | Brown
          4 | sanskar    | sanskar@example.com       | 2003-06-19 | goyal
          2 | yashu      | yashu@example.com         | 2003-04-20 | bharadwaj
(5 rows)


university_db=> DELETE (2, 'yashu', 'bharadwaj', 'yashu@example.com', '2003-04-20');
ERROR:  syntax error at or near "("
LINE 1: DELETE (2, 'yashu', 'bharadwaj', 'yashu@example.com', '2003-...
               ^
university_db=> INSERT INTO students (student_id, first_name, last_name, email, dob)
university_db-> UPDATE (5, 'yashu', 'bharadwaj', 'yashu@example.com', '2003-04-20');
ERROR:  syntax error at or near "UPDATE"
LINE 2: UPDATE (5, 'yashu', 'bharadwaj', 'yashu@example.com', '2003-...
        ^
university_db=> UPDATE students
university_db-> SET age = 22
university_db-> SET age = 22;;
ERROR:  syntax error at or near "SET"
LINE 3: SET age = 22;
        ^
university_db=> UPDATE students
university_db-> SET student_id = 5
university_db-> WHERE first_name = 'yashu';
UPDATE 1
university_db=> SELECT * FROM STUDENT
university_db-> ;
ERROR:  relation "student" does not exist
LINE 1: SELECT * FROM STUDENT
                      ^
university_db=> SELECT * FROM STUDENTS ;
 student_id | first_name |           email           |    dob     | last_name
------------+------------+---------------------------+------------+-----------
          1 | Alice      | alice.smith@example.com   | 2003-05-15 | Smith
          2 | Bob        | bob.johnson@example.com   | 2002-08-22 | Johnson
          3 | Charlie    | charlie.brown@example.com | 2003-01-10 | Brown
          4 | sanskar    | sanskar@example.com       | 2003-06-19 | goyal
          5 | yashu      | yashu@example.com         | 2003-04-20 | bharadwaj
(5 rows)


university_db=> SELECT first_name, last_name, email FROM students;
 first_name | last_name |           email
------------+-----------+---------------------------
 Alice      | Smith     | alice.smith@example.com
 Bob        | Johnson   | bob.johnson@example.com
 Charlie    | Brown     | charlie.brown@example.com
 sanskar    | goyal     | sanskar@example.com
 yashu      | bharadwaj | yashu@example.com
(5 rows)


university_db=> SELECT * FROM students;SELECT * FROM students WHERE student_id = 1;
 student_id | first_name |           email           |    dob     | last_name
------------+------------+---------------------------+------------+-----------
          1 | Alice      | alice.smith@example.com   | 2003-05-15 | Smith
          2 | Bob        | bob.johnson@example.com   | 2002-08-22 | Johnson
          3 | Charlie    | charlie.brown@example.com | 2003-01-10 | Brown
          4 | sanskar    | sanskar@example.com       | 2003-06-19 | goyal
          5 | yashu      | yashu@example.com         | 2003-04-20 | bharadwaj
(5 rows)


 student_id | first_name |          email          |    dob     | last_name
------------+------------+-------------------------+------------+-----------
          1 | Alice      | alice.smith@example.com | 2003-05-15 | Smith
(1 row)


university_db=> SELECT first_name, last_name FROM students WHERE last_name = 'bharadwaj';
 first_name | last_name
------------+-----------
 yashu      | bharadwaj
(1 row)


university_db=>
university_db=> SELECT * FROM students WHERE dob >= '2003-01-01'; -- Students born in or after 2003
 student_id | first_name |           email           |    dob     | last_name
------------+------------+---------------------------+------------+-----------
          1 | Alice      | alice.smith@example.com   | 2003-05-15 | Smith
          3 | Charlie    | charlie.brown@example.com | 2003-01-10 | Brown
          4 | sanskar    | sanskar@example.com       | 2003-06-19 | goyal
          5 | yashu      | yashu@example.com         | 2003-04-20 | bharadwaj
(4 rows)


university_db=> SELECT * FROM students WHERE dob BETWEEN '2002-01-01' AND '2002-12-31'; -- Born in 2002
 student_id | first_name |          email          |    dob     | last_name
------------+------------+-------------------------+------------+-----------
          2 | Bob        | bob.johnson@example.com | 2002-08-22 | Johnson
(1 row)


university_db=> SELECT * FROM students WHERE first_name LIKE 'A%'
university_db-> ;
 student_id | first_name |          email          |    dob     | last_name
------------+------------+-------------------------+------------+-----------
          1 | Alice      | alice.smith@example.com | 2003-05-15 | Smith
(1 row)


university_db=> SELECT * FROM students WHERE first_name LIKE 'S%'
university_db-> SELECT * FROM students WHERE first_name LIKE 's%'
university_db-> ;
ERROR:  syntax error at or near "SELECT"
LINE 2: SELECT * FROM students WHERE first_name LIKE 's%'
        ^
university_db=> SELECT * FROM students WHERE first_name LIKE 's%';
 student_id | first_name |        email        |    dob     | last_name
------------+------------+---------------------+------------+-----------
          4 | sanskar    | sanskar@example.com | 2003-06-19 | goyal
(1 row)


university_db=>
university_db=> SELECT * FROM students WHERE email ILIKE '%.com'; -- Case-insensitive ends with .com
 student_id | first_name |           email           |    dob     | last_name
------------+------------+---------------------------+------------+-----------
          1 | Alice      | alice.smith@example.com   | 2003-05-15 | Smith
          2 | Bob        | bob.johnson@example.com   | 2002-08-22 | Johnson
          3 | Charlie    | charlie.brown@example.com | 2003-01-10 | Brown
          4 | sanskar    | sanskar@example.com       | 2003-06-19 | goyal
          5 | yashu      | yashu@example.com         | 2003-04-20 | bharadwaj
(5 rows)


university_db=> SELECT * FROM students WHERE first_name = 'Alice' AND last_name = 'Smith';
 student_id | first_name |          email          |    dob     | last_name
------------+------------+-------------------------+------------+-----------
          1 | Alice      | alice.smith@example.com | 2003-05-15 | Smith
(1 row)


university_db=> SELECT * FROM students WHERE student_id = 5 OR student_id = 3;
 student_id | first_name |           email           |    dob     | last_name
------------+------------+---------------------------+------------+-----------
          3 | Charlie    | charlie.brown@example.com | 2003-01-10 | Brown
          5 | yashu      | yashu@example.com         | 2003-04-20 | bharadwaj
(2 rows)


university_db=> SELECT * FROM students WHERE student_id IN (1, 3, 5);
 student_id | first_name |           email           |    dob     | last_name
------------+------------+---------------------------+------------+-----------
          1 | Alice      | alice.smith@example.com   | 2003-05-15 | Smith
          3 | Charlie    | charlie.brown@example.com | 2003-01-10 | Brown
          5 | yashu      | yashu@example.com         | 2003-04-20 | bharadwaj
(3 rows)


university_db=> INSERT INTO students (student_id, first_name, last_name, dob) VALUES (4, 'Diana', 'Prince', '2001-11-01');
INSERT 0 1
university_db=> select * from students;
 student_id | first_name |           email           |    dob     | last_name
------------+------------+---------------------------+------------+-----------
          1 | Alice      | alice.smith@example.com   | 2003-05-15 | Smith
          2 | Bob        | bob.johnson@example.com   | 2002-08-22 | Johnson
          3 | Charlie    | charlie.brown@example.com | 2003-01-10 | Brown
          4 | sanskar    | sanskar@example.com       | 2003-06-19 | goyal
          5 | yashu      | yashu@example.com         | 2003-04-20 | bharadwaj
          4 | Diana      |                           | 2001-11-01 | Prince
(6 rows)


university_db=> SELECT * FROM students WHERE email IS NULL;
 student_id | first_name | email |    dob     | last_name
------------+------------+-------+------------+-----------
          4 | Diana      |       | 2001-11-01 | Prince
(1 row)


university_db=> SELECT * FROM students WHERE email IS NOT NULL;
 student_id | first_name |           email           |    dob     | last_name
------------+------------+---------------------------+------------+-----------
          1 | Alice      | alice.smith@example.com   | 2003-05-15 | Smith
          2 | Bob        | bob.johnson@example.com   | 2002-08-22 | Johnson
          3 | Charlie    | charlie.brown@example.com | 2003-01-10 | Brown
          4 | sanskar    | sanskar@example.com       | 2003-06-19 | goyal
          5 | yashu      | yashu@example.com         | 2003-04-20 | bharadwaj
(5 rows)


university_db=> SELECT * FROM students;
 student_id | first_name |           email           |    dob     | last_name
------------+------------+---------------------------+------------+-----------
          1 | Alice      | alice.smith@example.com   | 2003-05-15 | Smith
          2 | Bob        | bob.johnson@example.com   | 2002-08-22 | Johnson
          3 | Charlie    | charlie.brown@example.com | 2003-01-10 | Brown
          4 | sanskar    | sanskar@example.com       | 2003-06-19 | goyal
          5 | yashu      | yashu@example.com         | 2003-04-20 | bharadwaj
          4 | Diana      |                           | 2001-11-01 | Prince
(6 rows)


university_db=> UPDATE STUDENT
university_db-> SET student_id = 6
university_db-> WHERE first_name = Diana;
ERROR:  relation "student" does not exist
LINE 1: UPDATE STUDENT
               ^
university_db=> UPDATE STUDENTS
university_db-> SET student_id = 6
university_db-> WHERE first_name = Diana;
ERROR:  column "diana" does not exist
LINE 3: WHERE first_name = Diana;
                           ^
university_db=> UPDATE STUDENTS
university_db-> SET student_id = 6
university_db-> WHERE first_name = 'Diana';
UPDATE 1
university_db=> SELECT
university_db->   student_id,
university_db->   first_name,       -- now appears second
university_db->   last_name,
university_db->   email,
university_db->   dob
university_db-> FROM students;
 student_id | first_name | last_name |           email           |    dob
------------+------------+-----------+---------------------------+------------
          1 | Alice      | Smith     | alice.smith@example.com   | 2003-05-15
          2 | Bob        | Johnson   | bob.johnson@example.com   | 2002-08-22
          3 | Charlie    | Brown     | charlie.brown@example.com | 2003-01-10
          4 | sanskar    | goyal     | sanskar@example.com       | 2003-06-19
          5 | yashu      | bharadwaj | yashu@example.com         | 2003-04-20
          6 | Diana      | Prince    |                           | 2001-11-01
(6 rows)


university_db=> select * from students ;
 student_id | first_name |           email           |    dob     | last_name
------------+------------+---------------------------+------------+-----------
          1 | Alice      | alice.smith@example.com   | 2003-05-15 | Smith
          2 | Bob        | bob.johnson@example.com   | 2002-08-22 | Johnson
          3 | Charlie    | charlie.brown@example.com | 2003-01-10 | Brown
          4 | sanskar    | sanskar@example.com       | 2003-06-19 | goyal
          5 | yashu      | yashu@example.com         | 2003-04-20 | bharadwaj
          6 | Diana      |                           | 2001-11-01 | Prince
(6 rows)


university_db=> UPDATE STUDENTS
university_db-> SET email = 'diana@gmail.com'
university_db-> WHERE student_id = 6;
UPDATE 1
university_db=> select * from students;
 student_id | first_name |           email           |    dob     | last_name
------------+------------+---------------------------+------------+-----------
          1 | Alice      | alice.smith@example.com   | 2003-05-15 | Smith
          2 | Bob        | bob.johnson@example.com   | 2002-08-22 | Johnson
          3 | Charlie    | charlie.brown@example.com | 2003-01-10 | Brown
          4 | sanskar    | sanskar@example.com       | 2003-06-19 | goyal
          5 | yashu      | yashu@example.com         | 2003-04-20 | bharadwaj
          6 | Diana      | diana@gmail.com           | 2001-11-01 | Prince
(6 rows)


university_db=> DELETE FROM students WHERE student_id = 6;
DELETE 1
university_db=> SELECT * FROM students ORDER BY first_name ASC;
 student_id | first_name |           email           |    dob     | last_name
------------+------------+---------------------------+------------+-----------
          1 | Alice      | alice.smith@example.com   | 2003-05-15 | Smith
          2 | Bob        | bob.johnson@example.com   | 2002-08-22 | Johnson
          3 | Charlie    | charlie.brown@example.com | 2003-01-10 | Brown
          4 | sanskar    | sanskar@example.com       | 2003-06-19 | goyal
          5 | yashu      | yashu@example.com         | 2003-04-20 | bharadwaj
(5 rows)


university_db=> ELECT * FROM students ORDER BY dob DESC;
ERROR:  syntax error at or near "ELECT"
LINE 1: ELECT * FROM students ORDER BY dob DESC;
        ^
university_db=> SELECT * FROM students ORDER BY dob DESC;
 student_id | first_name |           email           |    dob     | last_name
------------+------------+---------------------------+------------+-----------
          4 | sanskar    | sanskar@example.com       | 2003-06-19 | goyal
          1 | Alice      | alice.smith@example.com   | 2003-05-15 | Smith
          5 | yashu      | yashu@example.com         | 2003-04-20 | bharadwaj
          3 | Charlie    | charlie.brown@example.com | 2003-01-10 | Brown
          2 | Bob        | bob.johnson@example.com   | 2002-08-22 | Johnson
(5 rows)


university_db=> SELECT * FROM STUDENTS;
 student_id | first_name |           email           |    dob     | last_name
------------+------------+---------------------------+------------+-----------
          1 | Alice      | alice.smith@example.com   | 2003-05-15 | Smith
          2 | Bob        | bob.johnson@example.com   | 2002-08-22 | Johnson
          3 | Charlie    | charlie.brown@example.com | 2003-01-10 | Brown
          4 | sanskar    | sanskar@example.com       | 2003-06-19 | goyal
          5 | yashu      | yashu@example.com         | 2003-04-20 | bharadwaj
(5 rows)


university_db=> select * from students
university_db-> ;
 student_id | first_name |           email           |    dob     | last_name
------------+------------+---------------------------+------------+-----------
          1 | Alice      | alice.smith@example.com   | 2003-05-15 | Smith
          2 | Bob        | bob.johnson@example.com   | 2002-08-22 | Johnson
          3 | Charlie    | charlie.brown@example.com | 2003-01-10 | Brown
          4 | sanskar    | sanskar@example.com       | 2003-06-19 | goyal
          5 | yashu      | yashu@example.com         | 2003-04-20 | bharadwaj
(5 rows)


university_db=> SELECT * FROM students ORDER BY dob DESC;
 student_id | first_name |           email           |    dob     | last_name
------------+------------+---------------------------+------------+-----------
          4 | sanskar    | sanskar@example.com       | 2003-06-19 | goyal
          1 | Alice      | alice.smith@example.com   | 2003-05-15 | Smith
          5 | yashu      | yashu@example.com         | 2003-04-20 | bharadwaj
          3 | Charlie    | charlie.brown@example.com | 2003-01-10 | Brown
          2 | Bob        | bob.johnson@example.com   | 2002-08-22 | Johnson
(5 rows)


university_db=> select * from students WHERE student_id = 3 ;
 student_id | first_name |           email           |    dob     | last_name
------------+------------+---------------------------+------------+-----------
          3 | Charlie    | charlie.brown@example.com | 2003-01-10 | Brown
(1 row)


university_db=> SELECT * FROM students ORDER BY last_name DESC;
 student_id | first_name |           email           |    dob     | last_name
------------+------------+---------------------------+------------+-----------
          1 | Alice      | alice.smith@example.com   | 2003-05-15 | Smith
          2 | Bob        | bob.johnson@example.com   | 2002-08-22 | Johnson
          4 | sanskar    | sanskar@example.com       | 2003-06-19 | goyal
          3 | Charlie    | charlie.brown@example.com | 2003-01-10 | Brown
          5 | yashu      | yashu@example.com         | 2003-04-20 | bharadwaj
(5 rows)


university_db=> SELECT * FROM students ORDER BY last_name ACS;
ERROR:  syntax error at or near "ACS"
LINE 1: SELECT * FROM students ORDER BY last_name ACS;
                                                  ^
university_db=> SELECT * FROM students ORDER BY last_name ACSE;
ERROR:  syntax error at or near "ACSE"
LINE 1: SELECT * FROM students ORDER BY last_name ACSE;
                                                  ^
university_db=> SELECT * FROM students ORDER BY last_name AESC;
ERROR:  syntax error at or near "AESC"
LINE 1: SELECT * FROM students ORDER BY last_name AESC;
                                                  ^
university_db=> SELECT * FROM students ORDER BY last_name AESC;
ERROR:  syntax error at or near "AESC"
LINE 1: SELECT * FROM students ORDER BY last_name AESC;
                                                  ^
university_db=> SELECT * FROM students ORDER BY last_name ASCE;
ERROR:  syntax error at or near "ASCE"
LINE 1: SELECT * FROM students ORDER BY last_name ASCE;
                                                  ^
university_db=> SELECT * FROM students ORDER BY last_name ASC;
 student_id | first_name |           email           |    dob     | last_name
------------+------------+---------------------------+------------+-----------
          5 | yashu      | yashu@example.com         | 2003-04-20 | bharadwaj
          3 | Charlie    | charlie.brown@example.com | 2003-01-10 | Brown
          4 | sanskar    | sanskar@example.com       | 2003-06-19 | goyal
          2 | Bob        | bob.johnson@example.com   | 2002-08-22 | Johnson
          1 | Alice      | alice.smith@example.com   | 2003-05-15 | Smith
(5 rows)


university_db=> SELECT COUNT(*) AS total_students FROM students;
 total_students
----------------
              5
(1 row)


university_db=> SELECT COUNT(EMAIL) AS total_students FROM students;
 total_students
----------------
              5
(1 row)


university_db=> SELECT COUNT(DISTINCT last_name) AS total_students FROM students;
 total_students
----------------
              5
(1 row)


university_db=> SELECT MIN(dob) AS oldest_student_dob FROM students;R
 oldest_student_dob
--------------------
 2002-08-22
(1 row)


university_db-> SELECT MAX(dob) AS youngest_student FROM STUDENTS;
ERROR:  syntax error at or near "R"
LINE 1: R
        ^
university_db=> SELECT MAX(dob) AS youngest_student FROM STUDENT;
ERROR:  relation "student" does not exist
LINE 1: SELECT MAX(dob) AS youngest_student FROM STUDENT;
                                                 ^
university_db=> SELECT MAX(dob) AS youngest_student FROM STUDENT;S
ERROR:  relation "student" does not exist
LINE 1: SELECT MAX(dob) AS youngest_student FROM STUDENT;
                                                 ^
university_db-> SELECT MAX(dob) AS youngest_student FROM STUDENTS;
ERROR:  syntax error at or near "S"
LINE 1: S
        ^
university_db=> SELECT MAX(dob) AS youngest_student FROM STUDENTS;
 youngest_student
------------------
 2003-06-19
(1 row)


university_db=> SELECT avg(dob) AS youngest_student FROM STUDENT;S
ERROR:  relation "student" does not exist
LINE 1: SELECT avg(dob) AS youngest_student FROM STUDENT;
                                                 ^
university_db-> SELECT avg(dob) AS youngest_student FROM STUDENts;
ERROR:  syntax error at or near "S"
LINE 1: S
        ^
university_db=> SELECT avg(dob) AS youngest_student FROM STUDENTS;
ERROR:  function avg(date) does not exist
LINE 1: SELECT avg(dob) AS youngest_student FROM STUDENTS;
               ^
HINT:  No function matches the given name and argument types. You might need to add explicit type casts.
university_db=> SELECT SUM(dob) AS youngest_student FROM STUDENTS;
ERROR:  function sum(date) does not exist
LINE 1: SELECT SUM(dob) AS youngest_student FROM STUDENTS;
               ^
HINT:  No function matches the given name and argument types. You might need to add explicit type casts.
university_db=> SELECT AMSX(dob) AS youngest_student FROM STUDENTS;
ERROR:  function amsx(date) does not exist
LINE 1: SELECT AMSX(dob) AS youngest_student FROM STUDENTS;
               ^
HINT:  No function matches the given name and argument types. You might need to add explicit type casts.
university_db=> SELECT MAX(dob) AS youngest_student FROM STUDENTS;
 youngest_student
------------------
 2003-06-19
(1 row)


university_db=> SELECT MIN(dob) AS youngest_student FROM STUDENTS;
 youngest_student
------------------
 2002-08-22
(1 row)


university_db=> SELECT COUNT(EMAIL) AS total_students FROM students;
 total_students
----------------
              5
(1 row)


university_db=> SELECT COUNT(DISTINCT last_name) AS total_students FROM students;
 total_students
----------------
              5
(1 row)


university_db=> select * form students
university_db-> ;
ERROR:  syntax error at or near "form"
LINE 1: select * form students
                 ^
university_db=> select * from students
university_db-> ;
 student_id | first_name |           email           |    dob     | last_name
------------+------------+---------------------------+------------+-----------
          1 | Alice      | alice.smith@example.com   | 2003-05-15 | Smith
          2 | Bob        | bob.johnson@example.com   | 2002-08-22 | Johnson
          3 | Charlie    | charlie.brown@example.com | 2003-01-10 | Brown
          4 | sanskar    | sanskar@example.com       | 2003-06-19 | goyal
          5 | yashu      | yashu@example.com         | 2003-04-20 | bharadwaj
(5 rows)


university_db=> INSERT INTO students (student_id, first_name, last_name, email, dob)
university_db-> VALUES (6, 'kush', 'Smith', '2004-07-01');
ERROR:  INSERT has more target columns than expressions
LINE 1: ...NTO students (student_id, first_name, last_name, email, dob)
                                                                   ^
university_db=> INSERT INTO students (student_id, first_name, last_name, email, dob)
university_db-> VALUES (6, 'kush', 'Smith', '2004-07-01');
ERROR:  INSERT has more target columns than expressions
LINE 1: ...NTO students (student_id, first_name, last_name, email, dob)
                                                                   ^
university_db=> INSERT INTO students (student_id, first_name, last_name, email, dob)
university_db-> VALUES (6, 'kush', 'pradhan', '2004-07-01');
ERROR:  INSERT has more target columns than expressions
LINE 1: ...NTO students (student_id, first_name, last_name, email, dob)
                                                                   ^
university_db=> INSERT INTO students (student_id, first_name, last_name, dob)
university_db-> VALUES (6, 'kush', 'pradhan', '2004-07-01');
INSERT 0 1
university_db=> select * from students;
 student_id | first_name |           email           |    dob     | last_name
------------+------------+---------------------------+------------+-----------
          1 | Alice      | alice.smith@example.com   | 2003-05-15 | Smith
          2 | Bob        | bob.johnson@example.com   | 2002-08-22 | Johnson
          3 | Charlie    | charlie.brown@example.com | 2003-01-10 | Brown
          4 | sanskar    | sanskar@example.com       | 2003-06-19 | goyal
          5 | yashu      | yashu@example.com         | 2003-04-20 | bharadwaj
          6 | kush       |                           | 2004-07-01 | pradhan
(6 rows)


university_db=> select last_name
university_db-> count(*) AS number_of_students
university_db-> FROM STUDENTS
university_db-> GROUP BY last_name
university_db-> ;
ERROR:  syntax error at or near "("
LINE 2: count(*) AS number_of_students
             ^
university_db=> select last_name
university_db-> COUNT(*) AS number_of_students
university_db-> FROM STUDENTS
university_db-> GROUP BY last_name
university_db-> ;
ERROR:  syntax error at or near "("
LINE 2: COUNT(*) AS number_of_students
             ^
university_db=> select last_name,
university_db-> COUNT(*) AS number_of_students
university_db-> FROM STUDENTS
university_db-> GROUP BY last_name
university_db-> ;
 last_name | number_of_students
-----------+--------------------
 bharadwaj |                  1
 Johnson   |                  1
 pradhan   |                  1
 Smith     |                  1
 goyal     |                  1
 Brown     |                  1
(6 rows)


university_db=> select last_name,
university_db-> COUNT(*) AS number_of_students
university_db-> FROM STUDENTS ;
ERROR:  column "students.last_name" must appear in the GROUP BY clause or be used in an aggregate function
LINE 1: select last_name,
               ^
university_db=> select DOB,
university_db-> COUNT(*) AS NO_OF STUDENTS
university_db->
university_db-> FROM STUDENTS
university_db-> GROUP BY DOB;
ERROR:  syntax error at or near "STUDENTS"
LINE 2: COUNT(*) AS NO_OF STUDENTS
                          ^
university_db=> select DOB,
university_db-> COUNT(*) AS NO_OF_STUDENTS
university_db-> FROM STUDENTS
university_db-> GROUP BY DOB;
    dob     | no_of_students
------------+----------------
 2003-04-20 |              1
 2003-05-15 |              1
 2003-06-19 |              1
 2002-08-22 |              1
 2003-01-10 |              1
 2004-07-01 |              1
(6 rows)


university_db=> DROP TABLE STUDENTS;
DROP TABLE
university_db=> CREATE TABLE students (
university_db(> student_id SERIAL PRIMARY KEY,
university_db(> first_name VARCHAR(50) NOT NULL,
university_db(> last_name VARCHAR(50) NOT NULL,
university_db(> email VARCHAR(100) UNIQUE,
university_db(> DOB DATE);
CREATE TABLE
university_db=> INSERT INTO students (first_name, last_name, email, dob, enrollment_status)
university_db-> VALUES ('Alice', 'Smith', 'alice.smith@example.com', '2003-05-15', 'enrolled');
ERROR:  column "enrollment_status" of relation "students" does not exist
LINE 1: ...INTO students (first_name, last_name, email, dob, enrollment...
                                                             ^
university_db=> INSERT INTO students (first_name, last_name, email, dob, enrollment_status)
university_db-> VALUES ('Robert', 'Johnson', 'robert.j@example.com', '2002-08-22', 'enrolled');
ERROR:  column "enrollment_status" of relation "students" does not exist
LINE 1: ...INTO students (first_name, last_name, email, dob, enrollment...
                                                             ^
university_db=> INSERT INTO students (first_name, last_name, email, dob, enrollment_status)
university_db-> VALUES ('Charlie', 'Brown', 'charlie.brown@example.com', '2003-01-10', 'pending');
ERROR:  column "enrollment_status" of relation "students" does not exist
LINE 1: ...INTO students (first_name, last_name, email, dob, enrollment...
                                                             ^
university_db=> SELECT * FROM STUDENTS;
 student_id | first_name | last_name | email | dob
------------+------------+-----------+-------+-----
(0 rows)


university_db=> INSERT INTO students (first_name, last_name, email, dob, enrollment_status)
university_db-> VALUES ('Alice', 'Smith', 'alice.smith@example.com', '2003-05-15', 'enrolled');
ERROR:  column "enrollment_status" of relation "students" does not exist
LINE 1: ...INTO students (first_name, last_name, email, dob, enrollment...
                                                             ^
university_db=> VALUES ('Alice', 'Smith', 'alice.smith@example.com', '2003-05-15');
 column1 | column2 |         column3         |  column4
---------+---------+-------------------------+------------
 Alice   | Smith   | alice.smith@example.com | 2003-05-15
(1 row)


university_db=> INSERT INTO students (first_name, last_name, email, dob)
university_db-> VALUES ('Robert', 'Johnson', 'robert.j@example.com', '2002-08-22'),
university_db-> ('Charlie', 'Brown', 'charlie.brown@example.com', '2003-01-10');
INSERT 0 2
university_db=> SELECT * FROM STUDENTS;
 student_id | first_name | last_name |           email           |    dob
------------+------------+-----------+---------------------------+------------
          1 | Robert     | Johnson   | robert.j@example.com      | 2002-08-22
          2 | Charlie    | Brown     | charlie.brown@example.com | 2003-01-10
(2 rows)


university_db=> CREATE TABLE courses (
university_db(>     course_id SERIAL PRIMRY KEY,
university_db(>     course_name VARCHAR(100) NOT NULL UNIQUE,
university_db(>     credits INTEGER CHECK (credits > 0 AND credits < 10) -- Example of CHECK
university_db(> );
ERROR:  syntax error at or near "PRIMRY"
LINE 2:     course_id SERIAL PRIMRY KEY,
                             ^
university_db=>
university_db=> INSERT INTO courses (course_name, credits) VALUES ('Introduction to SQL', 3);
ERROR:  relation "courses" does not exist
LINE 1: INSERT INTO courses (course_name, credits) VALUES ('Introduc...
                    ^
university_db=> INSERT INTO courses (course_name, credits) VALUES ('Database Design', 4);
ERROR:  relation "courses" does not exist
LINE 1: INSERT INTO courses (course_name, credits) VALUES ('Database...
                    ^
university_db=> INSERT INTO courses (course_name, credits) VALUES ('Web Development', 3);
ERROR:  relation "courses" does not exist
LINE 1: INSERT INTO courses (course_name, credits) VALUES ('Web Deve...
                    ^
university_db=> INSERT INTO courses (course_name, credits) VALUES ('Data Structures', 4);
ERROR:  relation "courses" does not exist
LINE 1: INSERT INTO courses (course_name, credits) VALUES ('Data Str...
                    ^
university_db=> CREATE TABLE courses (
university_db(>     course_id SERIAL PRIMRY KEY,
university_db(>     course_name VARCHAR(100) NOT NULL UNIQUE,
university_db(>     credits INTEGER CHECK (credits > 0 AND credits < 10) -- Example of CHECK
university_db(> );
ERROR:  syntax error at or near "PRIMRY"
LINE 2:     course_id SERIAL PRIMRY KEY,
                             ^
university_db=> CREATE TABLE courses (
university_db(>     course_id SERIAL PRIMARY KEY,
university_db(>     course_name VARCHAR(100) NOT NULL UNIQUE,
university_db(>     credits INTEGER CHECK (credits > 0 AND credits < 10) -- Example of CHECK
university_db(> );
CREATE TABLE
university_db=> INSERT INTO courses (course_name, credits) VALUES ('Introduction to SQL', 3);
INSERT 0 1
university_db=> INSERT INTO courses (course_name, credits) VALUES ('Database Design', 4);
INSERT 0 1
university_db=> INSERT INTO courses (course_name, credits) VALUES ('Web Development', 3);
INSERT 0 1
university_db=> INSERT INTO courses (course_name, credits) VALUES ('Data Structures', 4);
INSERT 0 1
university_db=> CREATE TABLE enrollments (
university_db(>     enrollment_id SERIAL PRIMARY KEY,
university_db(>     student_id INTEGER NOT NULL,
university_db(>     course_id INTEGER NOT NULL,
university_db(>     enrollment_date DATE DEFAULT CURRENT_DATE, -- Sets default if not specified
university_db(>     grade CHAR(1) CHECK (grade IN ('A', 'B', 'C', 'D', 'F', 'W', NULL)),
university_db(> CONSTRAINT fk_student
university_db(>         FOREIGN KEY (student_id)
university_db(>         REFERENCES students(student_id)
university_db(>         ON DELETE CASCADE,
university_db(> CONSTRAINT fk_course
university_db(>         FOREIGN KEY (course_id)
university_db(>         REFERENCES courses(course_id)
university_db(>         ON DELETE RESTRICT,
university_db(> UNIQUE (student_id, course_id)
university_db(> );
CREATE TABLE
university_db=> INSERT INTO enrollments (student_id, course_id, grade)
university_db-> VALUES (1, 1, 'A');
INSERT 0 1
university_db=> INSERT INTO enrollments (student_id, course_id) VALUES (1, 2);
INSERT 0 1
university_db=> INSERT INTO enrollments (student_id, course_id, grade) VALUES (2, 1, 'B');
INSERT 0 1
university_db=> SELECT * FROM enrollments
university_db-> ;
 enrollment_id | student_id | course_id | enrollment_date | grade
---------------+------------+-----------+-----------------+-------
             1 |          1 |         1 | 2025-05-30      | A
             2 |          1 |         2 | 2025-05-30      |
             3 |          2 |         1 | 2025-05-30      | B
(3 rows)


university_db=> SELECT * FROM cousre;
ERROR:  relation "cousre" does not exist
LINE 1: SELECT * FROM cousre;
                      ^
university_db=> SELECT * FROM cousres;
ERROR:  relation "cousres" does not exist
LINE 1: SELECT * FROM cousres;
                      ^
university_db=> SELECT * FROM courses;
 course_id |     course_name     | credits
-----------+---------------------+---------
         1 | Introduction to SQL |       3
         2 | Database Design     |       4
         3 | Web Development     |       3
         4 | Data Structures     |       4
(4 rows)


university_db=>               
```
