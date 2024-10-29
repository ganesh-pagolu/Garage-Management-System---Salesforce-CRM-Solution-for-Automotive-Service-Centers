# Garage Management System - Salesforce CRM Solution for Automotive Service Centers

## Overview

The **Garage Management System (GMS)** is a comprehensive CRM solution built on Salesforce, designed specifically for automotive service centers. This system streamlines customer management, appointment scheduling, service tracking, and billing, creating a centralized platform that efficiently handles the customer lifecycle—from initial booking to post-service feedback.

## Demonstration

[Garage Management System Demo Video]()

Watch my Youtube video above for a complete demonstration of the Garage Management System's features and functionality.

## Key Features

* **Customer details:**
    * Store and manage customer details including contact information, service history, and preferences.
    * Access comprehensive service records for customer insights and tailored service.

* **Appointment:**
    * Schedule and manage appointments with mechanics.
    * Automated reminders and notifications to reduce no-shows.
    * Integrated calendar to optimize working time.

* **Service Records:**
    * Track detailed service information including service type, parts used, and associated costs.
    * Link service records to specific customer appointments for easy tracking and reference.

* **Billing details:**
    * Generate and manage billing details, linking them to service records.
    * Track payment status and send timely payment reminders.
    * Automated invoice generation and email notifications for a streamlined payment process.

* **Feedback:**
    * Collect and manage customer feedback post-service.
    * Track ratings and comments to enhance service quality.
    * Analyze feedback trends for continuous improvement.

## Technical Architecture

### Custom Objects

* `Customer details`
* `Appointment`
* `Service Records`
* `Billing details & Feedback`

### Object Relationships

* `Appointment` → `Customer details` (Lookup)
* `Service Records` → `Appointment` (Lookup)
* `Billing details and feedback` → `Service Records` (Lookup)

### Automation

* **Flows:**
    * **Record-trigger Flow:** Manages customer verification, appointment, and reminder notifications.
    * **Amount Update Flow:** Automatically generates a billing record upon service completion and sends payment reminders.
    * **Email Alert Flow:** Sends a feedback request to customers post-service.

* **Approval Processes:** Approvals for high-value repairs or additional services, with manager-based routing and email notifications for approvals and rejections.

* **Apex Triggers:**
    * **`AmountDistributionTrigger`:** Validates business hours for appointment and Automatically calculates service costs and updates billing status upon payment.

### User Interface

* **Lightning Components:**
    * Custom Lightning App: "Garage Management System"
    * Custom Home Page for easy navigation and quick access to customer and appointment details.
    * Streamlined navigation with essential tabs and dashboards for Sales person and managers.

## Setup Instructions

1. **Object Creation:**
    * Create `Customer details` and `Service Records` objects and data.
    * Create `Appointment`, `Billing details`, and `Feedback` objects.
    * Create relationship fields to link objects as needed.

2. **User Configuration:**
    * Set up profiles for Sales person and Managers.
    * Configure user permissions and hierarchies for different user roles.

3. **Flow Deployment:**
    * Deploy the `Record-trigger Flow`.
    * Deploy the `Amount update Flow`.
    * Deploy the `Email alert Flow`.

4. **Lightning App Setup:**
    * Deploy the `Garage Management System` Lightning App.
    * Configure home page layouts to suit user roles.
    * Assign app permissions to profiles.

## Custom Settings

### Billing details and Feedback 

* **Payment Status Values:** `Pending`, `Completed`
* **Service Type Values:** `Maintainance Service`, `Repair`, `Replacement Parts`
* **Rating for Service:** 1 (Poor) - 5 (Excellent)

## Features in Detail

### Appointment

1. Customer requests an appointment, entering their preferred date and time.
2. also provides the type of service required and provide details like vehicle number plate and other customer details.
3. Appointment is confirmed, and a reminder email is sent to the customer.

### Service details  and Billing

1. Here all services provided, parts replaced and others will be recorded.
2. Billing record is generated based on service type and labor, with costs calculated automatically.
3. Payment reminders are sent if the billing status is pending.

### Feedback Collection and Analysis

1. Feedback request is sent to the customer post-service.
2. Customer submits their feedback, which is recorded and linked to their profile.
3. Negative feedback triggers a follow-up case for management review.

## System Requirements

* Salesforce Enterprise Edition or higher
* System Administrator profile for initial setup
* Service records and sales person licenses for end users

## Author

**Manohara Sai Subba Raju Golla**  
Gayatri Vidya Parishad College of Engineering (A), Visakhapatnam  
Roll Number: 21131A05D3<br>
Email: 21131A05D3@gvpce.ac.in  

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Acknowledgments

* Gayatri Vidya Parishad College of Engineering (A),
* Salesforce Development Team,
* Project Mentors and Guides.

---

*Note: This README is part of an SalesForce project demonstrating Salesforce CRM implementation for Garage Management System.*
