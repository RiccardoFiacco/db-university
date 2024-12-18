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

### quinto

SELECT *
FROM `exams`
WHERE `date` = '2020-06-20'
AND `hour` > '14:00:00';

### sesto

SELECT *
FROM `degrees`
WHERE `level` LIKE 'magistrale';

### settima

SELECT COUNT(*)
FROM `departments`;

###  ottava
SELECT COUNT(*)
FROM `teachers`
WHERE `phone` IS NULL;

### nona
INSERT INTO `students` (`degree_id`, `name`, `surname`, `date_of_birth`, `fiscal_code`, `enrolment_date`, `registration_number`, `email`)
VALUES (61, 'riccardo', 'fiacco', '2000-12-17', '0487523YBF402534', '2019-09-21', '6', 'rf@gmail.it')

### decima
UPDATE `teachers`
SET `office_address` = "126"
WHERE `name` LIKE "Pietro" AND `surname` LIKE "Rizzo"