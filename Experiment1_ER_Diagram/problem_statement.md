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

| Entity | Attributes (PK, FK) | Notes |
|---|---|---|
| MEMBER | member_id (PK), name, membership_type, start_date | Stores member details |
| PROGRAM | program_id (PK), program_name | Stores fitness program details |
| TRAINING_SESSION | session_id (PK), session_date | Stores training session details |
| TRAINER | trainer_id (PK), trainer_name | Stores trainer details |
| ATTENDANCE | attendance_id (PK), status | Stores attendance details |
| PAYMENT | payment_id (PK), payment_name, amount | Stores payment details |


### Relationships and Constraints


| Relationship | Cardinality | Participation | Notes |
|---|---|---|---|
| MEMBER - JOINS - PROGRAM | M:N | Partial | A member can join multiple programs |
| MEMBER - BOOKS - TRAINING_SESSION | 1:M | Partial | A member can book multiple training sessions |
| TRAINING_SESSION - TRAINER | M:1 | Total | A trainer can handle multiple training sessions |
| PROGRAM - ASSIGN_TO - TRAINER | M:N | Partial | A program can have multiple trainers |
| TRAINING_SESSION - HAS - ATTENDANCE | 1:1 | Total | Each training session has attendance |
| MEMBER - MAKES - PAYMENT | 1:M | Partial | A member can make multiple payments |

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

<img width="1060" height="717" alt="Screenshot 2026-09-09 203220" src="https://github.com/user-attachments/assets/e2e9aafb-5c6d-4811-8d5a-583dc8e3ebed" />


## Entities and Attributes

| Entity | Attributes (PK, FK) | Notes |
|---|---|---|
| MEMBER | Member_ID (PK), Name, Age, DOB, Phone_No, Email | Stores library member details |
| BOOKS | Book_ID (PK), Title, Author, Category | Stores book details |
| LOAN | Loan_ID (PK), Loan_Date, Return_Date, Member_ID (FK), Book_ID (FK) | Stores book lending details |
| FINE | F_ID (PK), Fine_Date, Amount, Paid_Status, Loan_ID (FK) | Stores overdue fine details |
| EVENTS | Event_ID (PK), Event_Name, Duration, Event_Date | Stores library event details |
| SPEAKERS | Speaker_ID (PK), Speaker_Name | Stores event speaker/author details |
| ROOMS | Room_ID (PK), Room_Name, Capacity | Stores library room details |
| REGISTRATION | Reg_ID (PK), Reg_Date, Member_ID (FK), Event_ID (FK) | Stores event registration details |

## Relationships and Constraints

| Relationship | Cardinality | Participation | Notes |
|---|---|---|---|
| MEMBER - BORROWS - LOAN | 1 : N | Member: Partial, Loan: Total | A member can borrow many books |
| LOAN - FOR - BOOKS | N : 1 | Loan: Total, Book: Partial | Each loan is for one book |
| LOAN - GENERATES - FINE | 1 : 0..1 | Loan: Partial, Fine: Total | Fine is generated for overdue loans |
| EVENTS - HAS - SPEAKERS | 1 : N | Event: Total, Speaker: Partial | An event has one or more speakers |
| EVENTS - REGISTER - REGISTRATION | 1 : N | Event: Partial, Registration: Total | Members can register for events |
| MEMBER - BELONGS TO - REGISTRATION | 1 : N | Member: Partial, Registration: Total | A member can have many registrations |
| EVENTS - HELD IN - ROOMS | N : 1 | Event: Total, Room: Partial | An event is held in one room |


## Assumptions

- Each member has a unique Member_ID.
- Each book has a unique Book_ID.
- A member can borrow multiple books.
- Each loan is associated with one member and one book.
- A fine is generated only for an overdue loan.
- Each event has at least one speaker.
- A member can register for multiple events.
- Each event is held in one room.
- A room can be used for multiple events at different times.
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
