# Fitness-Influencer-Coaching-Platform

## Overview

This project is a database design for an online fitness coaching platform.
Initially, coaching was done through Instagram and video calls, but as the number of clients increased, there was a need for a proper system to manage everything in one place.

This database helps manage trainers, clients, plans, subscriptions, sessions, payments, and progress tracking in a structured way.

---

## Main Idea

The platform allows:

* Trainers to create fitness plans
* Clients to purchase and follow those plans
* Sessions and consultations to be scheduled
* Progress to be tracked regularly
* Payments, discounts, and refunds to be handled

The design focuses on keeping everything organized and scalable.

---

## Core Entities

### Users

Stores both trainers and clients.
A role field is used to differentiate between them.

### Plans

Created by trainers. Each plan includes details like duration, price, and description.

### Subscriptions

Connects clients with plans.
This helps track which client purchased which plan and for how long.

### Sessions

Used to schedule consultations or live classes between trainer and client.

### Check-ins

Clients submit regular updates about their progress.

### Trainer Notes

Trainers give feedback based on client check-ins.

### Payments

Stores all payment-related information for subscriptions.

---

## Advanced Features Added

To make the system more practical and closer to real-world applications, the following features were added by me:

### Health Metrics

Tracks measurable data like weight, BMI, body fat, and calories.

### Streak System

Tracks user consistency such as workout streak or check-in streak.

### Coupons and Discounts

Allows users to apply discount codes while purchasing plans.

### Refund System

Handles refund requests when a client cancels a subscription.

---

## Relationships Overview

* One trainer can create multiple plans
* One client can purchase multiple plans over time
* One plan can be purchased by many clients
* A subscription connects a client and a plan
* One client can have many sessions and check-ins
* Each check-in can have trainer feedback
* Payments are linked to subscriptions
* Refunds are linked to payments

---

## Design Decisions

* Users are stored in a single table for simplicity and scalability
* Subscriptions are used to handle many-to-many relationships between clients and plans
* Check-ins and health metrics are stored separately to keep subjective and objective data clean
* Extra features like coupons, refunds, and streaks are added as separate tables to maintain modularity

---

## Conclusion

This database design provides a complete structure for an online fitness coaching platform.
It covers both basic functionality and advanced real-world features while keeping the design clean and scalable.

The system can be further expanded in the future by adding features like chat, notifications, or content libraries.
