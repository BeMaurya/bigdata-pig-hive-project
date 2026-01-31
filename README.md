# Pig and Hive Big Data Project

This repository contains a complete **Big Data implementation project**
using **Apache Hadoop, Apache Hive, and Apache Pig**.  
The project demonstrates how large datasets can be stored, processed,
queried, and analyzed efficiently using the Hadoop ecosystem.

This project was developed as part of the **MCA curriculum** and focuses on
practical implementation rather than theory alone.

---

## 🚀 Technologies Used

- **Java JDK 8**
- **Apache Hadoop 2.7.7**
- **Apache Hive 3.1.1**
- **Apache Pig 0.17.0**
- **HDFS (Hadoop Distributed File System)**

---

## 📂 Project Structure
```text
pig-hive-bigdata-project/
│
├── README.md
│
├── docs/
│ └── Pig_and_Hive_Project_Report.pdf
│
├── hive/
│ ├── create_database_and_tables.hql
│ ├── load_data.hql
│ ├── queries.hql
│
├── pig/
│ ├── load_data.pig
│ ├── analysis.pig
│ ├── join_operations.pig
│
├── data/
│ ├── AUTHOR_DATA.txt
│ ├── BOOK_DATA.txt
│
└── screenshots/
├── hive_output.png
├── pig_output.png
```

---

## 📊 Dataset Description

### 1️⃣ AUTHOR_DATA.txt
Contains information about authors.

| Field Name   | Description |
|-------------|-------------|
| AUTHOR_ID   | Unique author identifier |
| AUTHOR_NAME | Name of the author |

### 2️⃣ BOOK_DATA.txt
Contains information about books.

| Field Name   | Description |
|-------------|-------------|
| BOOK_ID     | Unique book identifier |
| BOOK_TITLE  | Title of the book |
| PUBLISHER   | Publisher name |
| NO_OF_BOOK  | Number of books |
| AUTHOR_ID   | Author reference |

---

## 🐝 Hive Operations

The following operations are performed using **HiveQL**:

- Database creation
- Table creation
- Loading data into Hive tables
- Filtering records
- Sorting data
- Group By operations
- Inner Join, Left Join, Right Join, Full Outer Join

### Example Hive Query
```sql
SELECT PUBLISHER, COUNT(*) 
FROM BOOK 
GROUP BY PUBLISHER;
```

## 🐷 Pig Operations

Apache Pig is used for data flow processing and analytics.

Operations include:

- Loading data using PigStorage

- Projection and filtering

- Grouping data

- Aggregation using SUM()

- Join operations

- Storing processed output

### Example Pig Script

```sql
grouped = GROUP book BY author_id;
result = FOREACH grouped GENERATE group, SUM(book.no_of_book);
DUMP result;
```

## ⚙️ How to Run the Project
```text
Step 1: Start Hadoop Services

start-all.cmd

Step 2: Run Hive
hive
Execute .hql files from the hive/ directory.
Step 3: Run Pig
pig -x local
Execute .pig scripts from the pig/ directory.
```

## 🎯 Project Objectives

Understand Hadoop ecosystem architecture

Perform SQL-like operations using Hive

Perform data flow analysis using Pig

Execute joins and aggregations on large datasets

Gain hands-on experience with Big Data tools

## 👨‍💻 Author

Shubham Kumar
Big Data | Hadoop | Hive | Pig

## 📌 Note

This project is intended for educational and learning purposes.
It can be extended further using:

- HBase

- Sqoop

- Spark

- Real-world datasets

## ⭐ If you find this project helpful, feel free to star the repository!

---

## 🔥 Why This README Is Strong
- Looks **professional**
- Clear **folder structure**
- Recruiter-friendly
- Not “college-copy-paste”
- Shows **hands-on Big Data skills**

## If you want next:
- I can **convert your entire PDF into clean `.hql` and `.pig` files**
- Or **review your GitHub profile** to match this project
- Or write a **resume project description** from this repo

Just say the word 👌


