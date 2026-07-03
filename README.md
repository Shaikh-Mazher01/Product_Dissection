# Product_Dissection

## 📌 Project Overview
A deep-dive data architecture project focused on reverse-engineering Amazon’s transactional core. This repository features a highly normalized, production-grade relational database design built from scratch, ensuring data integrity, optimized query execution, and explicit resilience against security vulnerabilities.

## 🛠️ Tech Stack & Core Skills
* **Database:** SQL / PostgreSQL (or MySQL)
* **Design Tools:** ERD Tools (e.g., dbdiagram.io, Lucidchart)
* **Core Competencies:** Data Architecture, Database Schema Design, 3NF Normalization, ER Modeling, Database Security (Anti-SQLi)

## 🏗️ Schema Architecture
The database features an **8-entity relational schema** structured in Third Normal Form (3NF) to eliminate data redundancy:
1. `Users` (Authentication & Profile details)
2. `Products` (Inventory, pricing, and category mapping)
3. `Orders` (Master transaction log)
4. `Order_Items` (Granular product-to-order mapping)
5. `Payments` (Transaction status, methods, and tokens)
6. `Cart` (Active session state tracking)
7. `Reviews` (User-generated ratings and feedback loops)
8. `Sellers` (Merchant inventory allocation)

## 🔒 Security & Data Integrity Features
* **Strict Constraints:** Enforces explicit `FOREIGN KEY` cascades, `NOT NULL` validations, and data-type boundary checks.
* **SQL Injection (SQLi) Defense:** Schema blueprints and operational views are structured specifically to abstract direct table access and support parameterized queries, neutralizing common web vulnerability attack vectors.

## 🚀 How to Use
1. Review the conceptual design in `/docs/ERD_Diagram.png`.
2. Run the initialization script to build the architecture:
   ```sql
   📁 database_init.sql
