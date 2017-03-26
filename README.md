## Learning Resoruces
[Primary key and foreign key](https://www.w3schools.com/sql/sql_foreignkey.asp)
[Baseball schema](http://seanlahman.com/files/database/readme2014.txt)



## Schema

Table names:

City, Department, Location, Employee, Employee_Department, Project, Assigned

View names:

Department_View, Employee_View

Attribute names:

empID, deptID, projID, role, title, budget, funds, deptName, firstName, midName, lastName, job, salary, streetNum, streetName, postCode, cityName

Additional Notes:

Attribute types should comply with those in createTables-lab2.sql.  Eg. Use VARCHAR(100) for streetNum otherwise, tests may fail.
If a person does not have a midName, it should be specified as NULL.
migrate.sql in the starter pack contains the guidelines for adding the BCNF-compliant data.
Submission Deadline: Tue, 28 Mar at 11:59 PM.

While performing the BCNF decomposition for Assignment 2 Part 1, please consider an additional implicit functional dependency "postCode uniquely determines cityName". 


While creating the tables for Assignment 2 Part 1, Please follow the below order of attributes.

empID, deptID, projID, role, title, budget, funds, deptName, firstName, midName, lastName, job, salary, streetNum, streetName, postCode, cityName

Assinged
empID, projID, role
empID foriegn key
projID foriegn key

Employee_department
empID, deptID
primarykey empID, deptID

Employee
empID, firstName, midName, lastName, job, salary
empID primary key


Project
primarykey projID

Department
deptID, deptName
deptID => deptName

Location
deptID, postCode, streetNum, streetName
deptID, postCode => streetNum, streetName

City
cityName, postCode
postCode => cityName