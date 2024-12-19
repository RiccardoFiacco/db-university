### prima query

SELECT *
FROM `students`
WHERE `date_of_birth` LIKE '1990-%-%';

### seconda query

SELECT *
FROM `courses`
WHERE `cfu` > 10;

### terza query


SELECT *, TIMESTAMPDIFF(YEAR, `date-of-birth`, CURRDATE())
FROM `students`
WHERE TIMESTAMPDIFF(YEAR, `date-of-birth`, CURRDATE())>30

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

### undicesima
DELETE
FROM `students`
WHERE `fiscal_code` LIKE '0487523YBF402534'

### QUERY GROUP BY
### prima
SELECT COUNT(*) as "numero ", `enrolment_date` as "data"
FROM `students`
GROUP BY `enrolment_date`

### seconda
SELECT COUNT(*) as "insegnanti", `office_number` as "numero ufficio"
FROM `teachers`
GROUP BY `office_number`

### terza
SELECT AVG(`vote`) as "media", `exam_id` as 'esame'
FROM `exam_student`
group by `exam_id`

### quarta
SELECT COUNT(*) as "totale corsi", `department_id` as "id dipartimento"
FROM `courses` AS `C`
JOIN `degrees` AS `D`
ON `C`.`degree_id` = `D`.`id`
GROUP BY `D`.`department_id`

### QUERY JOIN
### prima
SELECT `S`.`name`, `S`.`surname`, `D`.`name`
FROM `students` AS `S`
JOIN `degrees` AS `D`
ON `S`.`degree_id` = `D`.`id`
WHERE `D`.`name` LIKE 'Corso di Laurea in Economia'