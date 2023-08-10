# Basic-Queries-Task-

## Introduction
A number of task was given to test my understanding of basic SQL syntax. The task required the creation of Databases and Tables using the MSSMS
## Problem Statements 
- Create a Database named “Students Record”
- Create the following tables in the database create
- Students Info  (Student ID, Gender, Name, Age, Subject)
- Health records (Student ID, Blood Group, Height, Weight)
- Performance (Student ID, Score, Grade)
- The ID has to be unique
- Where a student has no score, it should be ‘0’ by default
- Add a constraint that prevents the ID and Subject from taking null values
- Apply the following modifications to the table
- Change column name ‘’Subject” to ‘’Course” 
- Drop the “Age” column from the ‘Students Info’ table
- Select the employee table and show the data where city is Mumbai and Delhi. 
- Select the employee table where employee first name have both ‘a’ and ‘e’  in them. 
- Subset the employee table to have employee with date of birth above 1990
- Subset the salary table to show salaries less than 1 million and sort in an ascending order
- Modify email column of the employee table to contain just email without ‘@gmail.com’

## SQL Queries
1.  Create Database Students_Record
2.  Create Table Students_info(Student_ID int Unique not null, Gender varchar, Name varchar(50), Age int, Subjects varchar not null);
3.  Create Table Health_records(Student_ID int Unique not null, Blood_Group varchar, Height nvarchar, Weight int);
4.  Create Table Performance(Student_ID int Unique not null, Score varchar default 0, Grade nvarchar);
5.  EXEC sp_rename 'dbo.Students_info.Subjects', 'Course', 'COLUMN';
6.   Alter Table Students_info Drop column Age;
7.  Select * From Employee 
    Where city = 'Mumbai' or city = 'Delhi';
8.  SELECT * FROM Employee
    WHERE fname LIKE '%a%' AND fname LIKE '%e%';
9.  SELECT * FROM Employee
    Where date_of_birth >= '1990-01-01';
10. SELECT * FROM Salary
   WHERE Base < 1000000
   ORDER BY Base ASC;
