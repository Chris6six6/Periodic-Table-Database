# Periodic Table Database Fixer and Information Retrieval Script

This project involves fixing issues in the `periodic_table` database and creating a bash script to retrieve information about chemical elements from the database.

## Part 1: Database Fixes

### Database Changes
- Renamed the `weight` column to `atomic_mass`.
- Renamed the `melting_point` column to `melting_point_celsius` and the `boiling_point` column to `boiling_point_celsius`.
- Added the UNIQUE constraint to the `symbol` and `name` columns in the `elements` table.
- Added the NOT NULL constraint to the `symbol` and `name` columns in the `elements` table.
- Set the `atomic_number` column in the `properties` table as a foreign key referencing the column of the same name in the `elements` table.
- Created a `types` table to store the three types of elements, with a `type_id` column as the primary key and a `type` column to store the different types.
- Added three rows to the `types` table representing the three different types of elements.
- Added a `type_id` foreign key column to the `properties` table referencing the `type_id` column in the `types` table.
- Capitalized the first letter of all the `symbol` values in the `elements` table.
- Removed trailing zeros after decimals from each row of the `atomic_mass` column.

### Additional Changes
- Added the element with atomic number 9 (Fluorine) and atomic number 10 (Neon) to the database.

## Part 2: Git Repository Creation

- Created a `periodic_table` folder in the project directory and initialized it as a Git repository.
- Made several commits with meaningful messages for each change made in the database.

## Part 3: Bash Script Development

### Script Features
- Created a bash script named `element.sh` to retrieve information about chemical elements from the database.
- The script accepts an argument in the form of atomic number, symbol, or name of an element.
- It displays information about the given element.
- Shows an error message if the element does not exist in the database.
- Provides usage instructions if no argument is provided.
- Made the script executable.

### Usage
- Run `./element.sh` without arguments to get usage instructions.
- Run `./element.sh 1`, `./element.sh H`, or `./element.sh Hydrogen` to get information about Hydrogen.
- Run `./element.sh` with another element as input to get information about the given element.

## Repository Details
- The repository has a main branch with all the commits.
- Commits follow conventional messages starting with fix:, feat:, refactor:,
