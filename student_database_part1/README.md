# Students Database Insert Script

This project contains a Bash script that inserts data from `courses.csv` and `students.csv` into a PostgreSQL database named `students`.

## Files

* `insert_data.sh` - Script used to insert the data
* `courses.csv` - Contains majors and courses
* `students.csv` - Contains student information

## What the Script Does

The script clears the existing tables, reads the CSV files, and inserts data into the following tables:

* `students`
* `majors`
* `courses`
* `majors_courses`

It also connects majors and courses using the `majors_courses` junction table.

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

## Notes

Make sure the PostgreSQL database and tables are already created before running the script.
