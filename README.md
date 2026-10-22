# Campus Event Management System (CEMS)

**Software Engineering Lab - 5th Semester**

A web-based Campus Event Management System built using pure **HTML, CSS, and JavaScript**. The project is organized into two experiments, each containing three tasks, covering user authentication and event management workflows.

---

## Project Files

`
EMS/
|-- E1_Task1.html        -> Experiment 1 | Task 1: User Login
|-- E1_Task2.html        -> Experiment 1 | Task 2: Role-Based Access Control
|-- E1_Task3.html        -> Experiment 1 | Task 3: Password Recovery and Reset
|-- E2_Task1.html        -> Experiment 2 | Task 1: Event Registration
|-- E2_Task2.html        -> Experiment 2 | Task 2: Registration Dashboard
|-- E2_Task3.html        -> Experiment 2 | Task 3: Event Payment and Confirmation
|-- Final_Project.html   -> Combined workflow of all 6 tasks in sequence
`

> No frameworks, no libraries, no build tools. All files open directly in any browser.

---

## Experiment 1 - User Authentication

### Task 1: E1_Task1.html - User Login

A login form for students to sign in to their campus account.

**Features:**
- Email and password input fields
- Client-side credential validation
- Success / error feedback messages
- Demo credentials shown on-screen for testing

**Demo Credentials:**

| Field    | Value                 |
|----------|-----------------------|
| Email    | student@example.com   |
| Password | Student123            |

---

### Task 2: E1_Task2.html - Role-Based Access Control

A role-based dashboard that simulates access permissions for different user types.

**Features:**
- Dropdown to select a demo user role (Student / Organizer / Administrator)
- Dashboard panel showing features available per role
- Protected section access checker
- Real-time access granted / denied feedback

**Roles and Permissions:**

| Role          | Accessible Sections                              |
|---------------|--------------------------------------------------|
| Student       | Public Events, Student Section                   |
| Organizer     | Public Events, Organizer Section                 |
| Administrator | Public Events, Student, Organizer, Admin Section |

---

### Task 3: E1_Task3.html - Password Recovery and Reset

A complete forgot-password flow with three stages.

**Features:**
- Stage 1 - Request Reset Code: Enter a registered email to receive a 6-digit demo reset code (displayed on-screen)
- Stage 2 - Reset Password: Enter the reset code and a new password (min 8 characters, must match confirmation)
- Stage 3 - Test Login: Verify the new password works with the test login form
- Password is updated in-memory; reset code is invalidated after use

---

## Experiment 2 - Event Management

### Task 1: E2_Task1.html - Event Registration

Browse available campus events and register using a Student ID.

**Features:**
- Live stats: Total Events, Available Seats, My Registrations
- Event cards showing name, date, venue, and seat availability
- Seat count decrements on successful registration
- Prevents duplicate registrations for the same student and event
- Seat badge turns red when an event is full
- Personal registration history displayed at the bottom

**Available Events:**

| Event                    | Date         | Venue               | Seats |
|--------------------------|--------------|---------------------|-------|
| Hackathon 2026           | 15 Nov 2026  | Computer Lab        | 3     |
| Web Development Workshop | 18 Nov 2026  | Seminar Hall        | 2     |
| Annual Tech Fest         | 22 Nov 2026  | College Auditorium  | 3     |

---

### Task 2: E2_Task2.html - Registration Dashboard

An admin/organizer-style dashboard showing the status of all event registrations.

**Features:**
- Summary stats: Total Events, Confirmed Registrations, Available Seats
- Table view with columns: Event, Student, Seats Left, Payment Status, Registration Status, Action
- Confirm button to confirm pending registrations (blocked if payment is pending or no seats)
- Status pills: Confirmed (green) / Pending (yellow) / Failed (red)
- Live table update after each confirmation action

**Sample Data:**

| Event                    | Student | Payment | Initial Status |
|--------------------------|---------|---------|----------------|
| Hackathon 2026           | Rahul   | Paid    | Confirmed      |
| Web Development Workshop | Priya   | Pending | Pending        |
| Tech Fest                | Amit    | Free    | Confirmed      |

---

### Task 3: E2_Task3.html - Event Payment and Confirmation

A simulated payment gateway for completing event registration.

**Features:**
- Split layout: Event details panel + Payment form panel
- Student email input and payment method selection (UPI / Card / Net Banking)
- Simulated payment result (Success or Failure) selectable by the user
- Seat count decrements on successful payment
- Payment receipt displayed after success (Registration ID, Email, Method, Amount, Status)
- Pay button is disabled after a successful payment to prevent duplicate charges
- HTML-escape applied to all user inputs for security

**Event Details:**

| Field            | Value              |
|------------------|--------------------|
| Event            | Tech Fest 2026     |
| Date             | 15 November 2026   |
| Venue            | College Auditorium |
| Registration Fee | Rs. 500            |
| Student          | Rahul Sharma       |
| Registration ID  | CEMS-2026-101      |

---

## Final_Project.html - Complete Workflow

A single-page file that combines all six tasks in sequential order, representing the full end-to-end CEMS workflow.

**Layout:**
- Sticky top header with a live progress bar (Step X / 6)
- Fixed sidebar with step navigation grouped by experiment
  - E1 steps highlighted in purple
  - E2 steps highlighted in teal
  - Sidebar items turn green when a step is scrolled past
- Scroll-aware active sidebar highlighting
- Arrow connectors between each task to visualise the workflow
- Experiment separators clearly divide E1 and E2 sections
- All task JavaScript logic fully functional within the same page
- Responsive layout - sidebar hides on smaller screens

**Workflow Sequence:**

`
Step 1: User Login             (E1 - Task 1)
           |
           v
Step 2: Role-Based Access      (E1 - Task 2)
           |
           v
Step 3: Password Recovery      (E1 - Task 3)
           |
           v
Step 4: Event Registration     (E2 - Task 1)
           |
           v
Step 5: Registration Dashboard (E2 - Task 2)
           |
           v
Step 6: Payment and Confirmation (E2 - Task 3)
`

---

## How to Run

1. Download or clone the repository.
2. Open any .html file directly in a web browser (Chrome, Firefox, Edge, etc.).
3. No server, no installation, no dependencies required.

To view the complete workflow:

`
Open  Final_Project.html  in your browser
`

To view individual tasks:

`
E1_Task1.html  ->  Login
E1_Task2.html  ->  Role-Based Access
E1_Task3.html  ->  Password Recovery
E2_Task1.html  ->  Event Registration
E2_Task2.html  ->  Registration Dashboard
E2_Task3.html  ->  Payment
`

---

## Technologies Used

| Technology | Usage                           |
|------------|---------------------------------|
| HTML5      | Page structure and semantics    |
| CSS3       | Styling, layout, responsiveness |
| JavaScript | Logic, validation, DOM updates  |

> All data is stored in-memory (no database or backend). Refreshing the page resets all state.

---

## Notes

- All payment flows are simulated demos. No real money is charged.
- Reset codes are shown on-screen for testing purposes only. In production, these would be sent via email.
- Credentials and registration data exist only during the current browser session.

---

*Campus Event Management System - Software Engineering Lab, 5th Semester*
