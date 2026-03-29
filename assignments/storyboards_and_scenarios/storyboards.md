# Storyboard / Lo-Fi UI for the UWON Library System

## Overview

The storyboard represents a web-based integrated UWON library system that supports:

* login and role-based access
* global bibliographical search across all departments
* book details and availability
* reservation and loan actions
* inter-library access through partner universities
* librarian acquisition support
* e-journal and digital library access
* staff-user email communication

The storyboard is divided into screens that represent the main user journeys.

### Screen 1 – Login Page

```text
+------------------------------------------------------+
|                 UWON Library System                  |
+------------------------------------------------------+
| Username: [__________________________]               |
| Password: [__________________________]               |
|                                                      |
| [ Log In ]                                           |
|                                                      |
| Forgot password?                                     |
|                                                      |
| Users: Students / Faculty / Library Staff / Admin    |
+------------------------------------------------------+
```

This is the entry point to the system.
Users authenticate and receive access according to their role.

### Screen 2 – Home Dashboard

```text
+--------------------------------------------------------------+
| UWON Library System                              [Logout]    |
+--------------------------------------------------------------+
| Welcome, Alice Student                                       |
| Role: Student                                                |
+--------------------------------------------------------------+
| [ Search Library ]   [ My Loans ]   [ My Reservations ]      |
| [ E-Journals ]       [ Partner Libraries ]                   |
+--------------------------------------------------------------+
| Notifications:                                               |
| - Reserved book available for pickup                         |
| - Loan due in 2 days                                         |
+--------------------------------------------------------------+
```

This is the main landing page after login.
The options shown depend on the user role.

For example:

* students see search, reservations, loans, e-journals
* library staff also see acquisition and user registration
* admin sees system management features

### Screen 3 – Global Search Page

```text
+------------------------------------------------------------------+
| UWON Library System                                   [Logout]   |
+------------------------------------------------------------------+
| Search all UWON libraries and partner systems                    |
|                                                                  |
| Search term: [ real-time systems________________________ ] [Go]  |
|                                                                  |
| Filters:                                                         |
| [x] Books   [x] Journals   [x] Proceedings   [x] E-Journals      |
| Department: [ All Departments v ]                                |
| Availability: [ Any v ]                                          |
+------------------------------------------------------------------+
| Results:                                                         |
| 1. Real-Time Systems, Kopetz                                     |
|    Type: Book   Location: Engineering Library                    |
|    Status: Available                                             |
|                                                                  |
| 2. Real-Time Systems Design                                      |
|    Type: Book   Location: Computer Science Library               |
|    Status: Loaned Out                                            |
|                                                                  |
| 3. Journal of Embedded Systems                                   |
|    Type: E-Journal   Access: Online                              |
+------------------------------------------------------------------+
```

This screen solves one of the biggest current problems:

* search is no longer manual
* search is no longer restricted to one department
* search is no longer limited to opening hours

This screen is the main hub for discovery.

### Screen 4 – Resource Details Page

```text
+---------------------------------------------------------------+
| Resource Details                                   [Back]     |
+---------------------------------------------------------------+
| Title: Real-Time Systems                                     |
| Author: Hermann Kopetz                                       |
| Type: Book                                                   |
| Keywords: real-time, embedded systems, dependability         |
|                                                              |
| Copies:                                                      |
| - Engineering Library ........ Available                     |
| - CS Library ................. Loaned out                    |
|                                                              |
| Related services:                                            |
| [ Borrow ]   [ Reserve ]   [ Add to Favorites ]              |
|                                                              |
| Similar resources:                                           |
| - Real-Time Systems Design                                   |
| - Dependable Embedded Software                               |
+---------------------------------------------------------------+
```

This screen gives details about one selected item and lets the user act on it.

Possible actions depend on status:

* if available → borrow
* if unavailable → reserve
* if digital → open online

### Screen 5 – Reservation Confirmation

```text
+-----------------------------------------------------------+
| Reservation                                               |
+-----------------------------------------------------------+
| Title: Real-Time Systems Design                           |
| Status: Currently unavailable                             |
| Estimated return date: 2026-04-10                         |
|                                                           |
| [ Confirm Reservation ]   [ Cancel ]                      |
+-----------------------------------------------------------+
| Notification preference:                                  |
| [x] Email                                                 |
| [ ] SMS                                                   |
+-----------------------------------------------------------+
```

This screen supports reservation of unavailable items and adds automatic notification.

### Screen 6 – My Loans / My Reservations

```text
+----------------------------------------------------------------+
| My Account                                          [Back]     |
+----------------------------------------------------------------+
| Active Loans:                                                   |
| 1. Computer Architecture                     Due: 2026-04-03    |
| 2. Embedded Systems Design                   Due: 2026-04-08    |
|                                                                  |
| [ Renew Selected Loan ]                                         |
+----------------------------------------------------------------+
| Reservations:                                                   |
| 1. Real-Time Systems Design                Waiting              |
| 2. Journal Volume 2025                     Ready for Pickup     |
+----------------------------------------------------------------+
```

This screen gives the user traceability and self-service capability.

It helps enforce loan limits, due dates, and reminders.

### Screen 7 – Partner Library Search

```text
+----------------------------------------------------------------+
| Partner Libraries Search                            [Back]     |
+----------------------------------------------------------------+
| Search term: [ fault tolerance____________________ ] [Go]      |
|                                                                |
| Partner Results:                                               |
| 1. Fault-Tolerant Systems                                      |
|    University: East Wonderland University                      |
|    Status: Available                                           |
|    [ Request Inter-Library Loan ]                              |
|                                                                |
| 2. Digital Dependability Journal                               |
|    University: North Wonderland Institute                      |
|    Status: Digital Access Available                            |
|    [ Request Access ]                                          |
+----------------------------------------------------------------+
```

This screen supports interoperability with partner universities and reduces unnecessary purchases.

### Screen 8 – E-Journal / Digital Access Screen

```text
+--------------------------------------------------------------+
| E-Journal Access                                   [Back]    |
+--------------------------------------------------------------+
| Title: Journal of Embedded Systems                           |
| Access Type: UWON Subscription                               |
| Coverage: 2018 - Present                                     |
|                                                              |
| [ Open Article ]                                             |
| [ Browse Issues ]                                            |
| [ Export Citation ]                                          |
+--------------------------------------------------------------+
| Related Digital Libraries:                                   |
| - Wonderland National Digital Library                        |
| - Partner University Archive                                 |
+--------------------------------------------------------------+
```

This screen reflects the requirement for e-journals and digital libraries.

It also avoids the old problem where physical journal issues are unavailable while being bound.

### Screen 9 – Librarian Acquisition Screen

```text
+--------------------------------------------------------------------+
| Acquisition Management                                  [Logout]   |
+--------------------------------------------------------------------+
| Search proposed title: [ Advanced Avionics Software_______ ] [Go]  |
|                                                                    |
| Existing UWON Copies:                                              |
| - Engineering Library ........ 1 copy, low usage                   |
| - CS Library ................. 0 copies                            |
|                                                                    |
| Partner Availability:                                              |
| - East Wonderland University ........ Available                    |
|                                                                    |
| Suggested action:                                                  |
| [ ] Acquire new copy                                               |
| [x] Use inter-library agreement                                    |
|                                                                    |
| E-Seller Comparison:                                               |
| Seller A ..... $89 ..... Delivery 3 days ..... [Select]            |
| Seller B ..... $94 ..... Delivery 1 day ..... [Select]             |
|                                                                    |
| [ Submit Order ]                                                   |
+--------------------------------------------------------------------+
```

This screen supports smarter acquisition decisions and reduces duplicate or unnecessary purchases.

### Screen 10 – Staff Communication Screen

```text
+--------------------------------------------------------------+
| Message User                                      [Back]     |
+--------------------------------------------------------------+
| To: Alice Student                                            |
| Subject: Reserved Book Available                             |
|                                                              |
| Message:                                                     |
| [ Your reserved book is now available for pickup.        ]   |
| [ Please collect it within 3 working days.               ]   |
|                                                              |
| [ Send Email ]                                               |
+--------------------------------------------------------------+
```

This screen supports staff-user communication through email.

## How the Diagrams Connect

The storyboard flows as described below.

### Main User Flow

1. The user starts at the **Login Page**.
2. After successful authentication, the user enters the **Home Dashboard**.
3. From the dashboard, the user can go to the **Global Search Page**.
4. Selecting a search result opens the **Resource Details Page**.
5. From the details page:

   * if the item is available, the user may borrow it
   * if the item is unavailable, the user goes to the **Reservation Confirmation** screen
   * if the item is digital, the user goes to the **E-Journal / Digital Access** screen
6. The user can check current status in **My Loans / My Reservations**.

### External Resource Flow

1. If the searched resource is not available at UWON, the user can continue to the **Partner Library Search** screen.
2. From there, the user may request:

   * an inter-library loan
   * digital access from a partner institution

### Librarian Flow

1. A librarian logs in through the same **Login Page**.
2. The librarian reaches a role-specific **Home Dashboard**.
3. From there, the librarian opens the **Acquisition Management** screen.
4. The librarian compares current UWON holdings, partner availability, and e-seller options before submitting an order.
5. The librarian can also use the **Staff Communication** screen to contact users.

## Reflection

A storyboard like this is useful because it makes the proposed system concrete from the user’s perspective. It shows not only what functions exist, but also how a student, researcher, or librarian would move through the system to achieve goals such as searching for resources, borrowing books, reserving unavailable items, requesting inter-library loans, or acquiring new books.
