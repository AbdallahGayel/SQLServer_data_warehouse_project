# 🛒 Sales Data Warehouse & Analytics Project

Hello! Welcome to my project.

This repository shows how I built a **Data Warehouse** from scratch using SQL Server. The goal of this project was to take messy, raw sales data and turn it into clear, reliable insights that a business can actually use.

I acted as both a **Data Engineer** (building the system) and a **Data Analyst** (finding the answers).

---

## 🏗️ How I Built It (The Architecture)

I used a method called the **Medallion Architecture**. Think of it like a water filtration system, where the data gets cleaner as it moves through the layers:

![Data Architecture Diagram](docs/data_architecture.png)

### 1. 🥉 Bronze Layer (Raw Data)
* **What it is:** This is where the data lands first.
* **What I did:** I took data from CSV files (Source Systems) and loaded it into the database exactly as it was. Even if it had errors, I kept it here so I have a record of the original state.

### 2. 🥈 Silver Layer (Clean Data)
* **What it is:** This is the "Transformation" step.
* **What I did:** I cleaned the data here. This involves fixing date formats, removing duplicates, and making sure the naming is consistent. This data is much easier to read.

### 3. 🥇 Gold Layer (Business Data)
* **What it is:** The final step, ready for reporting.
* **What I did:** I organized the data into a **Star Schema** (Fact and Dimension tables). This makes it very fast to run reports and analyze sales numbers.

---

## 🎯 Project Goals

I didn't just write code; I wanted to solve business problems. This project answers three main questions:
* **Who are the customers?** (Understanding behavior)
* **What are we selling?** (Product performance)
* **How is the business growing?** (Sales trends over time)

---

## 🛠️ Tools I Used

I used industry-standard tools to build this free of cost:
* **SQL Server Express:** To store the database.
* **SSMS (SQL Server Management Studio):** To write the queries and manage the data.
* **Draw.io:** To draw the diagrams and plan the architecture before coding.
* **Git & GitHub:** To save my work and manage versions.

---

## 📂 How the Files are Organized

Here is a simple map of this repository so you can find what you need:

```
data-warehouse-project/
│
├── datasets/                           # Raw datasets used for the project (ERP and CRM data)
│
├── docs/                               # Project documentation and architecture details
│   ├── etl.drawio                      # Draw.io file shows all different techniquies and methods of ETL
│   ├── data_architecture.drawio        # Draw.io file shows the project's architecture
│   ├── data_catalog.md                 # Catalog of datasets, including field descriptions and metadata
│   ├── data_flow.drawio                # Draw.io file for the data flow diagram
│   ├── data_models.drawio              # Draw.io file for data models (star schema)
│   ├── naming-conventions.md           # Consistent naming guidelines for tables, columns, and files
│
├── scripts/                            # SQL scripts for ETL and transformations
│   ├── bronze/                         # Scripts for extracting and loading raw data
│   ├── silver/                         # Scripts for cleaning and transforming data
│   ├── gold/                           # Scripts for creating analytical models
│
├── tests/                              # Test scripts and quality files
│
├── README.md                           # Project overview and instructions
├── LICENSE                             # License information for the repository
├── .gitignore                          # Files and directories to be ignored by Git
└── requirements.txt                    # Dependencies and requirements for the project
```
---

## 🛠️ Tools Used
I used the following tools to complete this project:

- **SQL Server Express**: To host the database.
- **SQL Server Management Studio (SSMS)**: To write queries and manage the database.
- **Draw.io**: To design the database diagrams.
- **Git & GitHub**: For version control.

---

## 🚀 How to Run This Project
If you want to run this project on your own machine, follow these steps:

### Prerequisites
- Make sure you have **SQL Server** and **SSMS** installed.

### Steps
1. **Download Data**  
   Get the CSV files from the `datasets/` folder.

2. **Setup Database**  
   Create a new database in SQL Server.

3. **Run Scripts**  
   Execute the SQL scripts located in the `scripts/` folder in the following order:
   - `bronze/` — Load data  
   - `silver/` — Clean data  
   - `gold/` — Model data  

---

## 🛡️ License
This project is licensed under the **MIT License**.  
You are free to use it, learn from it, and modify it for your own portfolio.
