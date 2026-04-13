# Bookstore Database + Python CLI

**Name:** Xinyu

## Project Description
This project is a music-themed bookstore database built with SQLite and Python. It stores book categories and books in a relational database and provides a command-line interface (CLI) for users to interact with the bookstore.

The bookstore includes music-related categories such as biographies, learn-to-play books, music theory, and scores or collections. Users can browse the database, search for books, and manage book records through the CLI.

The program allows users to:
- view all categories
- view all books
- view books in a selected category
- search books by title
- add a new book
- update a book price
- delete a book

## Additional Feature
This project also includes one extra feature beyond the demo:
- search books by author

## Files Included
- `createTables.sql`
- `insertRows.sql`
- `bookstore.db`
- `bookstore_cli.py`
- `README.md`

## Database Structure

### Table: `category`
This table stores the book categories.

Columns:
- `categoryId` – unique ID for each category
- `categoryName` – name of the category
- `categoryImage` – image filename for the category

### Table: `book`
This table stores information about each book.

Columns:
- `bookId` – unique ID for each book
- `categoryId` – category ID linked to the `category` table
- `title` – title of the book
- `author` – author of the book
- `isbn` – ISBN number for the book
- `price` – price of the book
- `image` – image filename for the book
- `readNow` – indicates whether the book is marked as “read now” (`0` = no, `1` = yes)

The `book` table uses `categoryId` as a foreign key to connect each book to a category.

## How to Create the Database
Run the following commands in the terminal:

```bash
sqlite3 bookstore.db < createTables.sql
sqlite3 bookstore.db < insertRows.sql

```markdown
## How to Run the Python Program
After creating the database, run:

```bash
python3 bookstore_cli.py
