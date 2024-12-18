### prima query

SELECT *
FROM `students`
WHERE `date_of_birth` LIKE '1990-%-%';

### seconda query

SELECT *
FROM `courses`
WHERE `cfu` > 10;

### terza query


SELECT *
FROM `students`
WHERE `date_of_birth` > "1994-01-01"

### quarta 
SELECT *
FROM `courses`
WHERE `period` LIKE 'I semestre' 
AND `year` = 1 