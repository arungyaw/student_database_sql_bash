# Students Database

This project contains  two parts:
* `student_database_part1` - Script used to insert the data using a Bash script that inserts data from `courses.csv` and `students.csv` into a PostgreSQL database named `students`.
* `student_database_part2` - Scripts used to describe info about the students from `students.sql` database.


## Files

* `students.sql` - SQL file dump for students database

part_1

* `insert_data.sh` - Script used to insert the data
* `courses.csv` - Contains majors and courses
* `students.csv` - Contains student information

part_2

* `students_info.sh` - Script used to describe the data


## What the Script Does

* `insert_data.sh` : The script clears the existing tables, reads the CSV files, and inserts data into the following tables:

* `students`
* `majors`
* `courses`
* `majors_courses`

It also connects majors and courses using the `majors_courses` junction table.

* `students_info.sh` - Uses different SQL commands embedded in bash scripting to describe certain information about the students database.

## Database Username

Before running the script, update the PostgreSQL username in the script based on your own system.

Example:

```bash
PSQL="psql -X --username=your_username --dbname=students --no-align --tuples-only -c"
```


## How to Run

```bash
chmod +x insert_data.sh
./insert_data.sh
```
```bash
chmod +x students_info.sh
./insert_data.sh
```

## Notes

Make sure the PostgreSQL database and tables are already created before running the script.
