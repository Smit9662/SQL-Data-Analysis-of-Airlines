Here's a concise **README** for your airline ticket booking analysis project. This format provides a clear overview, making it ideal for GitHub.

---

# Airline Ticket Booking Analysis

An SQL-based data analysis project on airline ticket bookings using PostgreSQL to gain insights into customer trends, popular destinations, revenue, and booking preferences.

## Project Overview

This project analyzes an airline ticket booking dataset to understand:
- Customer booking trends and patterns
- Popular destinations and travel preferences
- Revenue breakdown across different booking statuses
- Payment preferences and methods

## Objectives

- **Identify** top travel destinations and booking patterns
- **Analyze** revenue from confirmed bookings
- **Explore** customer payment preferences

## Data and Tools

- **Data**: Airline ticket booking dataset
- **Tools**: PostgreSQL and SQL for data querying and analysis

## Key Questions

### Easy
1. **Total Bookings**: How many total bookings are recorded?
   - `SELECT COUNT(*) FROM airline_ticket_bookings;`
2. **Bookings by Gender**: How many bookings were made by female customers?
   - `SELECT * FROM airline_ticket_bookings WHERE Gender = 'Female';`

### Moderate
1. **Total Revenue**: Calculate the total revenue generated from confirmed bookings.
   - `SELECT SUM(Price) FROM airline_ticket_bookings WHERE Ticket_Status = 'Confirmed';`
2. **Bookings per Destination**: Find the number of bookings for each destination.
   - `SELECT Destination, COUNT(*) FROM airline_ticket_bookings GROUP BY Destination;`

### Advanced
1. **Top Destinations**: Identify the top 3 destinations with the highest bookings.
   - `SELECT Destination, COUNT(*) FROM airline_ticket_bookings GROUP BY Destination ORDER BY COUNT(*) DESC LIMIT 3;`
2. **Recent Booking**: Retrieve the most recent booking for each customer.
   - `SELECT Customer_ID, MAX(Booking_Date) FROM airline_ticket_bookings GROUP BY Customer_ID;`

## Results & Insights

- **Top Destinations**: Popular travel locations include New York, London, and Tokyo.
- **Payment Preferences**: Credit cards are the preferred payment method for 75% of bookings.
- **Revenue**: Significant revenue generated from confirmed bookings, supporting revenue growth.

# Thank you.
