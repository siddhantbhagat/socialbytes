# socialbytes
assisment_test

Que 11. 

CREATE TABLE Student (ID INT PRIMARY KEY NOT NULL,
                      Name VARCHAR(20) NOT NULL,
                      Age INT NOT NULL,
                      Address VARCHAR(25) );

INSERT INTO Student (ID, Name, Age, Address) VALUES
(1, 'Siddhant', 28, 'Yavalmal'),
(2, 'Aniket', 30, 'Pune'),
(3, 'Pooja', 25, 'Mumbai'),
(4, 'nishant', 23, 'Nagpur'),
(5, 'Vivek', 40, 'delhi');

Que 12.

SELECT Name FROM Student Order by Age Limit 1 ;

Que 13.

SELECT P.FirstName, P.Lastname , A.City , A.State From Person as p join Address as A on P.Person.Id == A.Person.Id.

que 14.

SELECT DISTINCT Age FROM Student ORDER BY Age DESC LIMIT 1 Offset 1;

que 15.
SELECT DISTINCT Salary FROM Employee ORDER BY Salary DESC LIMIT 1 OFFSET (n - 1);

QUE 16.
SELECT Company, PERCENTILE_CONT(0.5) WITHIN GROUP (ORDER BY Salary) AS MedianSalary FROM Employee GROUP BY Company;

Que 17.
SELECT 
    EmployeeID,
    Month,
    SUM(Salary) OVER (PARTITION BY EmployeeID ORDER BY Month DESC ROWS BETWEEN 2 PRECEDING AND 1 PRECEDING) AS CumulativeSum
FROM SalaryData
ORDER BY EmployeeID ASC, Month DESC;

que 18.



