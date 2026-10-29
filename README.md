# ⚽ PLAYTOGETHER PROJECT - Sports Ground Booking System

> A complete MySQL 8.0 database project for managing sports grounds, slots, bookings, payments and audit records.



# 📌 Project Overview
---
PLAYTOGETHER is designed to digitize sports ground booking operations in Vizag. It handles users, sports grounds, available slots, bookings, payments and payment audit and automates business logic using advanced MySQL features.

<br>

# 🎯 Objectives
---
- To develop a centralized database for sports ground booking management.
- To automate slot allocation and prevent double-booking / overbooking.
- To maintain complete user history, bookings, and payment records.
- To generate revenue reports and ground occupancy reports easily.
- To reduce manual work for ground owners using Views, Procedures and Triggers.
- To ensure data integrity using Foreign Keys and Constraints.

<br>

# ✨ Features
---
- *6 Normalized Tables* - 3NF compliant design
- *Relationships* - Proper Foreign Keys linking all modules
- *Views* - For ground overview, booking details, payment summary, ground booking summary
- *Stored Procedures* - For getting all bookings, filter by sport and price, bookings by ground
- *Triggers* - Auto-validate payment amount, auto-audit payment updates/deletes, auto-release slot on cancellation
- *ENUM & Constraints* - For sport type, slot status, booking status, payment status, ground status

<br>

# 🗄️ Database Structure (6 Tables)
---

### 1. Users - Player / User details
- Stores name, phone, email

### 2. SportsGrounds - Ground details
- Stores ground name, sport type (Football/Cricket/Badminton/Tennis), location, hourly rate, capacity, status

### 3. Slots - Available time slots for each ground
- Stores ground_id, slot date, start time, end time, slot status (Available/Booked) with UNIQUE constraint on ground+date+time

### 4. Bookings - Booking history
- Links user, slot with booking date, status (Pending/Confirmed/Cancelled/Completed), total amount

### 5. Payments - Booking payments
- Stores booking_id, amount, method (UPI/Card/NetBanking/Cash), status (Pending/Success/Failed), payment date

### 6. Payment_Audit - Payment audit log
- Stores payment_id, action type, old status, new status, amount, action time - auto-filled via triggers

<br>

# 🚀 How to Run
---
1.  Clone this repo:
    git clone https://github.com/ajaypinapatruni-commits/PLAYTOGETHER_PROJECT.git
2.  Open MySQL Workbench
3.  Create database and run the full file:
    SOURCE PlayTogether_BedspaceV2_Format.sql;
    -- OR Run PART 1 to PART 11 step by step

<br>

# ⚠️ Limitations
---
- Currently backend-only project (No Frontend UI / Website yet).
- Payment gateway integration is not included, only payment records.
- No user authentication / login system.
- Notification system (SMS/Email alerts for booking confirmation) not implemented.
- Slot availability check depends on manual update + trigger, no real-time locking.

<br>

# 🔮 Future Enhancements
---
- Develop a Web Application using React + Node.js for ground owners and players.
- Add User Login for Owners and Players with Role-Based Access.
- Integrate Online Payment Gateway (UPI, Razorpay, Stripe) for instant booking.
- Add Real-time Slot Availability Dashboard with Calendar View and Charts.
- Implement Automated Booking Reminders via Email / SMS.
- Add Ground Ratings, Reviews and Photos Upload Feature.
- Mobile App for Players to Book Grounds, Split Payments and Invite Friends.

<br>

# 🏁 Conclusion
---
The PLAYTOGETHER project successfully demonstrates how MySQL can be used to solve real-world sports ground management problems. By using 6 normalized tables, foreign keys, CHECK constraints, indexes, views, procedures and triggers, the system ensures data accuracy and prevents manual errors like double booking. This project is a strong foundation that can be scaled into a full-stack product for Vizag and other cities.

<br>

# 👨‍💻 Author
---
** <br>
GitHub: <br>
Location: Visakhapatnam, Andhra Pradesh <br>
Project: PlayTogether - Sports Ground Booking System