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

<img width="866" height="722" alt="Screenshot 2026-08-29 220149" src="https://github.com/user-attachments/assets/90f5bdc6-874c-427a-9005-83dc759a5d05" />


### Entities and Attributes

```
### Entities and Attributes

| Entity | Attributes (PK, FK) | Notes |
|---|---|---|
| MEMBER | member_id (PK), name, membership_type, start_date | Stores member details |
| PROGRAM | program_id (PK), program_name | Stores fitness program details |
| TRAINING_SESSION | session_id (PK), session_date | Stores training session details |
| TRAINER | trainer_id (PK), trainer_name | Stores trainer details |
| ATTENDANCE | attendance_id (PK), status | Stores attendance details |
| PAYMENT | payment_id (PK), payment_name, amount | Stores payment details |
```

### Relationships and Constraints

```
| Relationship | Cardinality | Participation | Notes |
|---|---|---|---|
| MEMBER - JOINS - PROGRAM | M:N | Partial | A member can join multiple programs |
| MEMBER - BOOKS - TRAINING_SESSION | 1:M | Partial | A member can book multiple training sessions |
| TRAINING_SESSION - TRAINER | M:1 | Total | A trainer can handle multiple training sessions |
| PROGRAM - ASSIGN_TO - TRAINER | M:N | Partial | A program can have multiple trainers |
| TRAINING_SESSION - HAS - ATTENDANCE | 1:1 | Total | Each training session has attendance |
| MEMBER - MAKES - PAYMENT | 1:M | Partial | A member can make multiple payments |
```

### Assumptions

- Each member has a unique member_id.
- Each program has a unique program_id.
- Each trainer has a unique trainer_id.
- Each training session has a unique session_id.
- A member can join multiple programs.
- A program can have multiple trainers.
- A member can book multiple training sessions.
- A trainer can handle multiple training sessions.
- Each training session has one attendance record.
- A member can make multiple payments.
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
*Paste or attach your diagram here*  
![ER Diagram](er_diagram_restaurant.png)

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

## Instructions for Students

1. Complete **all three scenarios** (A, B, C).  
2. Identify entities, relationships, and attributes for each.  
3. Draw ER diagrams using **draw.io / diagrams.net** or hand-drawn & scanned.  
4. Fill in all tables and assumptions for each scenario.  
5. Export the completed Markdown (with diagrams) as **a single PDF**
