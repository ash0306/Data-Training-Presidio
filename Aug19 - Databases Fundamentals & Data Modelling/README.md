# Databases - Fundamentals & Data Modelling

Got insights into basics of Databases and Data Modelling.

Worked with:
- CTE's
- Joins
- Stored Procidures
- Triggers
- SQL Server Agent
- Jobs

## Task

Write stored procedures and add triggers so that changes made in the `student_src` table is being reflected in the `student_tgt` table as per the constraints

#### Constraints

- When data is added to the `student_src` table then the data is also added to the `student_tgt` table
- When the data is updated in the `student_src` table then a new entry with the updated data is added to the `student_tgt` table
- When the data is removed from the `student_src` table then the data is soft-deleted from the `student_tgt` table


The task done can be found [here](./DataTrainingDay1.sql)