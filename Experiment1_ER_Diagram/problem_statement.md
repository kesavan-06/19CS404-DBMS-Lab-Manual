# ER Diagram Workshop – Submission Template

## Objective
To understand and apply ER modeling concepts by creating ER diagrams for real-world applications.

## Purpose
Gain hands-on experience in designing ER diagrams that represent database structure including entities, relationships, attributes, and constraints.

---

# Scenario A: City Fitness Club Management

**Business Context:**  
FlexiFit Gym wants a database to manage its members, trainers, and fitness programs.

**Requirements:**  
- Members register with name, membership type, and start date.  
- Each member can join multiple programs (Yoga, Zumba, Weight Training).  
- Trainers assigned to programs; a program may have multiple trainers.  
- Members may book personal training sessions with trainers.  
- Attendance recorded for each session.  
- Payments tracked for memberships and sessions.

### ER Diagram:
*Paste or attach your diagram here*  
![ER Diagram](er_diagram_fitness.png)

### Entities and Attributes

| Entity | Attributes (PK, FK) | Notes |
|--------|--------------------|-------|
|        |                    |       |
|        |                    |       |
|        |                    |       |
|        |                    |       |
|        |                    |       |

### Relationships and Constraints

| Relationship | Cardinality | Participation | Notes |
|--------------|------------|---------------|-------|
|              |            |               |       |
|              |            |               |       |
|              |            |               |       |

### Assumptions
- 
- 
- 

---

# Scenario B: City Library Event & Book Lending System

**Business Context:**  
The Central Library wants to manage book lending and cultural events.

**Requirements:**  
- Members borrow books, with loan and return dates tracked.  
- Each book has title, author, and category.  
- Library organizes events; members can register.  
- Each event has one or more speakers/authors.  
- Rooms are booked for events and study.  
- Overdue fines apply for late returns.

### ER Diagram:
*Paste or attach your diagram here*  
![ER Diagram](er_diagram_library.png)

### Entities and Attributes

| Entity | Attributes (PK, FK) | Notes |
|--------|--------------------|-------|
|        |                    |       |
|        |                    |       |
|        |                    |       |
|        |                    |       |
|        |                    |       |

### Relationships and Constraints

| Relationship | Cardinality | Participation | Notes |
|--------------|------------|---------------|-------|
|              |            |               |       |
|              |            |               |       |
|              |            |               |       |

### Assumptions
- 
- 
- 

---

---

# Scenario C: Restaurant Table Reservation & Ordering

**Business Context:**  
A popular restaurant wants to manage reservations, orders, and billing.

**Requirements:**  
- Customers can reserve tables or walk in.  
- Each reservation includes date, time, and number of guests.  
- Customers place food orders linked to reservations.  
- Each order contains multiple dishes; dishes belong to categories (starter, main, dessert).  
- Bills generated per reservation, including food and service charges.  
- Waiters assigned to serve reservations.

### ER Diagram:
<img width="4512" height="2040" alt="Kesavan_ERworksop" src="https://github.com/user-attachments/assets/a40cd65e-f157-415c-be00-56ed5142a37b" />


### Entities and Attributes

| Entity      | Attributes (PK, FK)                                                                                       | Notes                              |
| ----------- | --------------------------------------------------------------------------------------------------------- | ---------------------------------- |
| Customer    | **Customer_ID (PK),** Customer_Name, Phone                                                                | Restaurant customers               |
| Reservation | **Reservation_ID (PK),** Reservation_Date, Reservation_Time, Guests, **Customer_ID (FK), Waiter_ID (FK)** | Table reservations                 |
| Order       | **Order_ID (PK),** Order_Date, Total_Amount, **Reservation_ID (FK)**                                      | Food orders placed by customers    |
| Dish        | **Dish_ID (PK),** Dish_Name, Price, Category                                                              | Menu items                         |
| Bill        | **Bill_ID (PK),** Food_Charges, Service_Charges, Total_Bill, **Reservation_ID (FK)**                      | Billing details                    |
| Waiter      | **Waiter_ID (PK),** Waiter_Name, Shift                                                                    | Restaurant staff serving customers |

### Relationships and Constraints

| Relationship                   | Cardinality        | Participation       | Notes                                                                       |
| ------------------------------ | ------------------ | ------------------- | --------------------------------------------------------------------------- |
| Customer makes Reservation     | One-to-Many (1:M)  | Partial             | A customer may have multiple reservations.                                  |
| Reservation places Order       | One-to-Many (1:M)  | Total (Order)       | Each order belongs to one reservation.                                      |
| Order contains Dish            | Many-to-Many (M:N) | Total (Order)       | An order may contain multiple dishes, and a dish can appear in many orders. |
| Reservation assigned to Waiter | Many-to-One (M:1)  | Total (Reservation) | Each reservation is served by one waiter.                                   |
| Reservation generates Bill     | One-to-One (1:1)   | Total               | One bill is generated for each completed reservation.                       |

### Assumptions
- Walk-in customers are also recorded as reservations.
- Each reservation is served by one waiter.
- One bill is generated for each reservation after all orders are completed.

---

## Instructions for Students

1. Complete **all three scenarios** (A, B, C).  
2. Identify entities, relationships, and attributes for each.  
3. Draw ER diagrams using **draw.io / diagrams.net** or hand-drawn & scanned.  
4. Fill in all tables and assumptions for each scenario.  
5. Export the completed Markdown (with diagrams) as **a single PDF**
