# Healthcare Insurance Claims Database

This repository contains the design and supporting materials for a relational database assignment. The database models sample healthcare insurance claims and related member, provider, diagnosis, and medicine information, with the aim of demonstrating how SQL can support basic analysis of claims data.

The project focuses on database design and querying. The fraud scores in the sample claims are illustrative; this is not a production claims system or a trained fraud-detection model.

## Database design

The schema consists of five tables:

- `members` stores member details such as name, gender, and age.
- `providers` stores provider names and statuses.
- `ICD_10_ailment_description` stores diagnosis codes, names, and descriptions.
- `claims_data` stores claim dates, types, billed and paid amounts, and an illustrative fraud score. Each claim references a member, provider, and diagnosis.
- `ailment_medicine` stores medicine names, dosages, and prices, linked to a diagnosis code.

Primary and foreign keys define the relationships between these entities. The report discusses the schema's normalization through first, second, and third normal form (1NF, 2NF, and 3NF).

## SQL topics demonstrated

The assignment materials cover table definitions, example inserts, and CSV import statements, along with queries using:

- `LIKE` and comparison filtering
- `LEFT JOIN`
- `GROUP BY` with `COUNT`
- `IN`
- `UPDATE`

The report includes examples and screenshots of query results. CSV import examples use MariaDB/MySQL `LOAD DATA LOCAL INFILE`; the database client and server must allow local infile for this method.

## Repository contents

- [Assignment report](3602723%20SQL%20Assignment.pdf) — database design, normalization discussion, SQL examples, and query results.
- [ERD image](ERD.drawio.png) and [editable ERD](ERD.drawio) — entity-relationship diagram.
- [`CSVs 2 import/`](CSVs%202%20import/) — sample CSV data for the database entities.
- [`Executed Statements Results/`](Executed%20Statements%20Results/) — screenshots of selected SQL query results.

The SQL statements are documented in the report