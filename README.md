# Periodic Table Database

This project is a bash script that queries a PostgreSQL database containing information about chemical elements from the periodic table. It provides details about elements based on user input.

## Project Description

The Periodic Table Database project consists of:
1. A PostgreSQL database with information about chemical elements.
2. A bash script that interacts with this database to provide element information.

The script accepts an argument (atomic number, symbol, or name of an element) and outputs specific information about that element.

## Script Functionality

The `element.sh` script:

- Accepts one command-line argument: atomic number, symbol, or name of an element.
- Queries the periodic_table database for information about the specified element.
- Outputs formatted information about the element, including:
  - Atomic number
  - Name
  - Symbol
  - Type (metal, metalloid, or nonmetal)
  - Atomic mass
  - Melting point
  - Boiling point

## Database Structure

The PostgreSQL database `periodic_table` contains the following tables:
- `elements`: Stores basic information about each element (atomic number, symbol, name).
- `properties`: Stores physical properties of elements (atomic mass, melting point, boiling point).
- `types`: Stores the types of elements (metal, metalloid, nonmetal).

## How to Use

1. Ensure you have PostgreSQL installed and the `periodic_table` database set up.
2. Run the script using one of the following formats:
   - `./element.sh <atomic_number>`
   - `./element.sh <symbol>`
   - `./element.sh <element_name>`

Example: `./element.sh 1` or `./element.sh H` or `./element.sh Hydrogen`

## Files in this Project

- `element.sh`: The main bash script for querying element information.
- `periodic_table.sql`: A SQL dump of the database structure and data.

## Database Modifications

As part of this project, the following modifications were made to the initial database:
- Renamed certain columns for clarity (e.g., 'weight' to 'atomic_mass').
- Added constraints to ensure data integrity.
- Normalized the database structure by creating a separate 'types' table.
- Capitalized element symbols and removed trailing zeros from atomic masses.

## Note

This project was completed as part of the freeCodeCamp Relational Database certification.
