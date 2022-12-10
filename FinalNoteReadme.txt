SELECT * fROM Jobs where BusinessTitle like '%programm%'

SELECT * fROM Jobs where BusinessTitle like '%engineer%'

SELECT SalaryRangeFrom, SalaryRangeTo
FROM Jobs
Where SalaryRangeFrom >= 100000

SELECT * FROM JOBS WHERE BusinessTitle LIKE '%attorney%'

trigger: CREATE TRIGGER alertjobtitle
AFTER INSERT on Agencys
BEGIN 
	INSERT into Jobs('JobID','Agency','BusinessTitle','SalaryRangeFrom','SalaryRangeTo')
	VALUES('NewJobID', 'Newagency', 'bustitle', 'Salform', 'salto');
END;

WITH AvgSal_cte
as
(SELECT
	avg(SalaryRangeFrom),
	avg(SalaryRangeTo)
FROM
	Jobs)
SELECT * FROM AvgSal_cte;

Data basese password: ncmc

