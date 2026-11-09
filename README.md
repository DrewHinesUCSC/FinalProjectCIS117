# Project Gutenberg Book Analyzer

A Python desktop application that retrieves book text from Project Gutenberg, analyzes word frequency, and stores results in a SQLite database for later lookup.

This project demonstrates Python application development, text processing, external data retrieval, relational database design, and desktop GUI development.

## Overview

The Project Gutenberg Book Analyzer allows users to enter a Project Gutenberg text URL, retrieve the book's contents, and identify the most frequently used words. Analysis results are saved locally, allowing users to search previously processed books by title without having to analyze them again.

The application combines a simple Tkinter interface with Python's built-in text-processing and database capabilities.

## Features

- **Book Retrieval:** Retrieves publicly available book text from Project Gutenberg URLs.
- **Text Processing:** Uses regular expressions to extract words and filter out shorter terms.
- **Word Frequency Analysis:** Uses Python's `Counter` to identify and rank the most frequently occurring words.
- **Persistent Storage:** Stores book titles and word-frequency results in a local SQLite database.
- **Book Lookup:** Retrieves previously analyzed books and displays their top 10 most frequent words.
- **Desktop Interface:** Provides a graphical interface built with Tkinter for entering URLs, processing books, and viewing results.

## Technologies

| Technology | Purpose |
|---|---|
| Python | Application logic and text processing |
| SQLite | Relational database and persistent storage |
| Tkinter | Desktop graphical user interface |
| Regular Expressions (`re`) | Word extraction and filtering |
| `collections.Counter` | Word-frequency analysis |
| `urllib.request` | Retrieving book text from URLs |

## How It Works

The application is organized into several core operations:

1. **Retrieve:** The user provides a Project Gutenberg URL, and the application retrieves the book's text.
2. **Process:** Regular expressions extract words from the retrieved content. Words are normalized to lowercase and counted.
3. **Store:** The book title and calculated word frequencies are saved in SQLite.
4. **Retrieve Results:** Users can search for a previously processed book by title and view its most frequent words.

## Database Design

The application uses SQLite with two related tables:

- **Books:** Stores book titles as unique records.
- **Frequencies:** Stores individual words and their corresponding frequency counts, associated with a book title.

This structure separates book metadata from its word-frequency results and allows previously processed data to be queried independently of the original text retrieval process.

## Running the Application

### Requirements

- Python 3
- Tkinter support

The project uses Python's standard library and SQLite, so no third-party Python packages are required.

### Setup

1. Clone the repository:

   ```bash
   git clone <https://github.com/DrewHinesUCSC/FinalProjectCIS117.git>
   ```

2. Navigate to the project directory:

   ```bash
   cd <FinalProjectCIS117>
   ```

3. Run the application:

   ```bash
   python3 <Gutenberg_Project>.py
   ```


The application uses a local SQLite database named `books.db` to store analyzed books and their word-frequency results.

## Project Background

Originally developed as a Python programming project, this application provided an opportunity to work with external text retrieval, data processing, relational database operations, and graphical user interface development.

It reflects an interest in building practical applications that combine data processing with persistent storage and an accessible user experience.

---

**Author:** Andrew (Drew) Hines  
**GitHub:** [github.com/DrewHinesUCSC](https://github.com/DrewHinesUCSC)
