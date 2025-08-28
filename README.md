# Paris Transit Database Design

This project demonstrates the design and implementation of a relational database for a public transport management system.  
It covers the process from **conceptual modeling (ERD)** to **logical modeling (3NF)** and the final **Oracle SQL schema**.

---

## Project Overview
A transport operator required a database to manage officials, drivers, vehicles, trips, and training records.  
The database design aimed to:
- Translate business requirements into a **conceptual data model (ERD)**.  
- Normalize data structures to **3NF** to ensure efficiency and integrity.  
- Implement a relational schema in **Oracle SQL** with constraints.  
- Document key **business assumptions** that guided design decisions.  

---

## Deliverables
1. **Entity-Relationship Diagram (ERD)**  
   - Captures core entities (officials, drivers, vehicles, trips, training modules).  
   - See: [`ERD_Conceptual.png`](./ERD_Conceptual.png)  

2. **Logical Model (3NF)**  
   - Normalized relational tables with primary and foreign keys.  
   - See: [`Logical_Model_3NF.png`](./Logical_Model_3NF.png)  

3. **SQL Schema**  
   - [`schema.sql`](./schema.sql) includes:  
     - `CREATE TABLE` statements  
     - Primary/Foreign key constraints  
     - Column datatypes and integrity checks  

4. **Business Assumptions**  
   - Documented to clarify design decisions.  
   - See: [`assumptions.md`](./assumptions.md)  

---

## Key Business Assumptions (Highlights)
- Training modules last **1–5 days** and are valid for up to **10 months**.  
- Vehicles have fewer than **100 seats**; odometer readings capped below **100,000**.  
- Driver security level: **FULL (F)** or **RESTRICTED (R)** (default = Restricted).  
- Driver suspension status: **Suspended (S)** or **Not Suspended (N)** (default = Not Suspended).  
- Driver–Language is a **many-to-many relationship**, resolved with a bridge table.  
- Officials may or may not have assigned team members.  

(Full list available in [`assumptions.md`](./assumptions.md))  

---

## Skills Demonstrated
- **Data Modeling**: Entities, attributes, and relationships.  
- **Normalization**: Applied UNF → 1NF → 2NF → 3NF to optimize schema design.  
- **SQL DDL**: Built Oracle schema with tables, keys, and constraints.  
- **Business Analysis**: Applied realistic assumptions to align database with operations.  

---
This project highlights my ability to **design scalable, normalized relational databases** that support both operational needs and analytical reporting.
