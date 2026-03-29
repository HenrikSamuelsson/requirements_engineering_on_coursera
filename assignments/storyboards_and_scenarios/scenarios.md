# UWON Library System – Scenarios

10 scenarios in total, 5 normal and 5 abnormal. Normal scenarios describe expected system usage, while abnormal scenarios capture exceptional conditions and help define robustness, error handling, and system constraints.

## Normal Scenarios (Expected Behavior)

### Scenario N1 – User Searches and Borrows a Book

**Actor:** Student

**Description:**

1. The student logs into the system.
2. The student searches for a book.
3. The system returns available results across all departments.
4. The student selects an available copy.
5. The student requests to borrow the book.
6. The system verifies eligibility.
7. The loan is registered with a due date.
8. A confirmation email is sent.

### Scenario N2 – Book Reservation

**Actor:** Student

**Description:**

1. The student searches for a book.
2. The system shows that all copies are currently loaned out.
3. The student places a reservation.
4. The system registers the reservation.
5. The system notifies the student when the book becomes available.

### Scenario N3 – Librarian Acquires a Book

**Actor:** Library Staff

**Description:**

1. The librarian initiates an acquisition request.
2. The system checks existing copies across UWON.
3. The system suggests whether acquisition is needed.
4. The librarian proceeds with acquisition.
5. The system provides e-seller comparison.
6. The librarian selects a supplier.
7. The order is submitted online.

### Scenario N4 – Access to E-Journal

**Actor:** Researcher

**Description:**

1. The researcher logs in.
2. The researcher searches for a journal article.
3. The system identifies an available e-journal subscription.
4. The researcher accesses the article online.

### Scenario N5 – Inter-Library Loan Request

**Actor:** Faculty Member

**Description:**

1. The user searches for a book not available at UWON.
2. The system queries partner universities.
3. Available copies at external libraries are displayed.
4. The user requests an inter-library loan.
5. The system sends the request to the partner system.
6. The user is notified when the book is available.

## Abnormal Scenarios (Exceptional / Error Conditions)

### Scenario A1 – User Exceeds Borrowing Limit

**Actor:** Student

**Description:**

1. The student attempts to borrow a book.
2. The system checks current loans.
3. The system detects that the user has exceeded the allowed limit.
4. The request is denied.
5. The system displays an error message explaining the restriction.

### Scenario A2 – Book Marked Available but Not Found

**Actor:** Library Staff

**Description:**

1. A student tries to locate a book marked as available.
2. The book is not found on the shelf.
3. The librarian reports the inconsistency.
4. The system flags the item as “missing”.
5. An investigation process is initiated.

### Scenario A3 – Unauthorized Access Attempt

**Actor:** Unauthorized User

**Description:**

1. A user attempts to access restricted functionality (e.g., acquisition module).
2. The system checks user authorization.
3. The user lacks sufficient permissions.
4. Access is denied.
5. The system logs the attempt.

### Scenario A4 – External Library System Unavailable

**Actor:** Researcher

**Description:**

1. A user searches for a book not available at UWON.
2. The system attempts to contact partner universities.
3. The external system is unavailable.
4. The system informs the user of the issue.
5. The system suggests retrying later.

### Scenario A5 – Overdue Book Not Returned

**Actor:** Student

**Description:**

1. A borrowed book reaches its due date.
2. The book is not returned.
3. The system sends reminder notifications.
4. The user still does not return the book.
5. The system applies penalties (e.g., suspension of borrowing privileges).
