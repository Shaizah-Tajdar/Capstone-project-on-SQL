# ✈️ Airline Database Project

## 🗂️ Overview

**Airline Database** is a relational database schema that models a real-world airline booking and flight management system. It captures the complete journey from booking to boarding and handles key entities such as tickets, flights, aircrafts, airports, and seat allocation.

This project serves as a foundational resource for learning database design, normalization, and querying for aviation systems.

---

## 🎯 Purpose

The aim of this project is to:

- Simulate a real-world airline reservation and boarding system
- Practice SQL queries for multi-table joins, aggregations, and constraints
- Understand relationships between bookings, flights, passengers, and aircrafts
- Explore data integrity and validation through schema design

---

## 🧱 Core Entities & Relationships

- **Bookings**: A booking can include multiple passengers (each with a ticket)
- **Tickets**: Tied to specific passengers and include one or more flight segments
- **Flights**: Represent a specific trip between two airports; same flight number may operate on different dates
- **Airports**: Departure and arrival points for flights
- **Aircrafts**: Aircraft models with predefined seating layouts
- **Seats**: Defined based on aircraft model and travel class
- **Boarding Passes**: Issued during check-in, link tickets to flights and seat numbers

---

## 🗺️ Schema Highlights

- **One-to-Many**: A booking → multiple tickets
- **Many-to-Many**: A ticket ↔ multiple flight segments (via `ticket_flights`)
- **Unique Constraints**: Prevents double-booking of seats via `boarding_passes`
- **Assumptions**:
  - All passengers are treated as unique individuals
  - All tickets in a booking share the same flight segments
  - Every aircraft model has one cabin configuration

---

## 📊 Insights & Analysis

Here are some of the key insights derived through SQL queries on the AirlineDB:

### ✈️ Flights with Highest Range
- Identified **flight IDs** with the **maximum range between departure and arrival airports** based on geographical distance or flight duration.
- These represent the **longest operational routes** in the dataset.

### 🕒 Longest Flight Details
- Retrieved full details (flight ID, origin, destination, duration, aircraft type) of the **longest flight** in the system.
- Useful for operational and logistics planning or capacity analysis.

### 🛂 Tickets Without Boarding Passes
- Queried and listed **tickets where passengers never checked in**.
- Helps identify **missed flights**, **incomplete check-ins**, or system inconsistencies.

### 💰 Highest Paying Passengers (Monthly)
- Performed a **month-wise breakdown** to identify **top-paying passengers** based on total ticket value.
- Includes passenger name, ticket ID, amount paid, and acquisition month.
- Useful for tracking **high-value customers** and loyalty profiling.

---

These insights demonstrate the power of structured relational databases in supporting operational analytics, customer behavior analysis, and revenue optimization in the airline industry.

---

## 📁 Dataset architecture

<img width="566" alt="image" src="https://github.com/user-attachments/assets/0cce31a5-0e45-4613-9aeb-83d1c76ec77a" />
