
# ER Diagram Workshop – Submission Template

## Objective
To understand and apply ER modeling concepts by creating ER diagrams for real-world applications.

## Purpose
Gain hands-on experience in designing ER diagrams that represent database structure, including entities, relationships, attributes, and constraints.

---

# Scenario C: Restaurant Table Reservation & Ordering

**Business Context:**  
A popular restaurant wants to manage reservations, orders, and billing.

**Requirements:**
- Customers can reserve tables or walk in.
- Each reservation includes date, time, and number of guests.
- Customers place food orders linked to reservations.
- Each order contains multiple dishes; dishes belong to categories (starter, main, dessert).
- Bills are generated per reservation, including food and service charges.
- Waiters are assigned to serve reservations.

### ER Diagram

<img width="4512" height="2040" alt="Kesavan_ERworksop" src="https://github.com/user-attachments/assets/a40cd65e-f157-415c-be00-56ed5142a37b" />

### Entities and Attributes

| Entity | Attributes (PK, FK) | Notes |
|---|---|---|
| Customer | **Customer_ID (PK),** Customer_Name, Phone | Restaurant customers |
| Reservation | **Reservation_ID (PK),** Reservation_Date, Reservation_Time, Guests, **Customer_ID (FK), Waiter_ID (FK)** | Table reservations |
| Order | **Order_ID (PK),** Order_Date, Total_Amount, **Reservation_ID (FK)** | Food orders placed by customers |
| OrderItem | **OrderItem_ID (PK),** Quantity, Status, **Order_ID (FK), FoodItem_ID (FK)** | Individual food items in an order |
| FoodItem | **FoodItem_ID (PK),** Name, Description, Category, Price | Restaurant menu items |
| Bill | **Bill_ID (PK),** Food_Charges, Service_Charges, Total_Bill, Payment_Status, **Reservation_ID (FK)** | Billing and payment details |
| Waiter | **Waiter_ID (PK),** Waiter_Name, Shift | Restaurant staff serving customers |

### Relationships and Constraints

| Relationship | Cardinality | Participation | Notes |
|---|---|---|---|
| Customer makes Reservation | One-to-Many (1:M) | Partial | A customer may make multiple reservations. |
| Reservation places Order | One-to-Many (1:M) | Total (Order) | Each order belongs to one reservation. |
| Order contains FoodItem | Many-to-Many (M:N) | Total (Order) | An order can contain multiple food items, and a food item can appear in many orders. Implemented through OrderItem. |
| Reservation assigned to Waiter | Many-to-One (M:1) | Total (Reservation) | Each reservation is assigned to one waiter. |
| Reservation generates Bill | One-to-One (1:1) | Total | Each completed reservation generates one bill. |

### Assumptions
- Walk-in customers are also recorded as reservations.
- Each reservation is served by one waiter.
- One bill is generated for each reservation after all orders are completed.

---

## Instructions for Students

1. Complete **all three scenarios (A, B, C)**.
2. Identify entities, relationships, and attributes for each.
3. Draw ER diagrams using **draw.io / diagrams.net** or hand-draw and scan them.
4. Fill in all tables and assumptions for each scenario.
5. Export the completed Markdown (with diagrams) as **a single PDF**.
