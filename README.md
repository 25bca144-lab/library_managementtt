# College Library Management System

A MySQL 8.0 project for managing a college library. The database contains members, books, and issue/return records, with SQL queries, a stored procedure, and a trigger.

## Files

| File | Description |
|---|---|
| `library_management.sql` | Creates the database and tables, then contains project queries C2–C12, stored procedure C13, and trigger C14. |
| `sample.sql` | Inserts the sample records into the database. |
| `erd.png` | Entity Relationship Diagram (ERD) for the database. |
| `README.md` | Project overview and instructions. |

## Database structure

- **members** — member details (`member_id` is the primary key).
- **books** — book details (`book_id` is the primary key).
- **issues** — issue and return details (`issue_id` is the primary key; `member_id` and `book_id` are foreign keys).

A member can have many issue records, and a book can appear in many issue records.

## How to run

Use MySQL 8.0 or a compatible MySQL environment.

1. Run `library_management.sql` first. It creates the `librarydb` database and the three tables.
2. Run `sample.sql` to insert the sample members, books, and issue records.
3. Run the query sections in `library_management.sql` (C2–C12) to view the results.
4. The same file includes stored procedure C13 and trigger C14. Run those sections in a MySQL 8.0-compatible environment that supports stored procedures and triggers.

**Important:** Run `sample.sql` only once on a fresh database to avoid duplicate sample records. The query sections should be executed after the sample data has been inserted.

## Fine calculation

The fine is **₹2 per late day**. A `NULL` `return_date` indicates that the book has not yet been returned.
