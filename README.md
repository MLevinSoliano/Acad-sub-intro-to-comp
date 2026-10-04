# Acad-sub-intro-to-comp
Computer Repair Service Request Page

# TechFix — Computer Repair Services

## Project Context

**Project Title:** TechFix — Computer Repair Services
**Submitted by:** Undergraduate BSIT — 1st Year, Section C
**Submitted to:** *Proctor Name*
**Academic Level:** Bachelor of Science in Information Technology (BSIT), 1st Year
**Year:** 2026

---

## 1. Project Overview

**TechFix** is a front-end website concept for a computer repair and technical services business.

The website presents a fictional repair service where customers can:

* View available computer repair services
* See starting service prices
* Understand the repair process
* Describe a computer or device problem
* Select a preferred service
* Indicate service priority
* Request additional services
* Select a preferred repair date
* Submit a simulated repair request

The project is primarily a **front-end HTML and CSS implementation**. The form submission is currently simulated using a JavaScript `alert()` rather than being connected to a real database, server, email system, or booking system.

---

# 2. Technologies Used

The project primarily uses:

* **HTML5** — page structure and form elements
* **CSS3** — layout, styling, responsive design, colors, spacing, animations, and visual presentation
* **Basic JavaScript** — used for the simulated form submission alert
* **Responsive Web Design** — media queries are used to adapt the page to different screen sizes

No backend programming or database is currently implemented.

---

# 3. Prior Technical Background

Before working on this project, my technical background was primarily focused on introductory HTML and CSS concepts.

Topics I had previously encountered include:

### HTML

* HTML document structure
* Basic HTML tags
* Headings
* Paragraphs
* Links
* Tables
* Forms
* Input types
* Radio buttons
* Checkboxes
* Dropdown/select menus
* Textareas
* Buttons
* Labels
* Basic attributes such as `id`, `name`, `value`, `placeholder`, and `required`

### CSS

* External CSS files
* Basic selectors
* Colors
* Fonts
* Margins and padding
* Borders
* Width and height
* Basic positioning
* Basic layout concepts
* Some exposure to responsive design

### JavaScript

* Very limited/basic exposure
* Using an `alert()` for a simulated interaction

There are also some HTML/CSS concepts that I had previously encountered but cannot currently recall completely or confidently explain.

Therefore, this project should be understood as an **early-stage undergraduate front-end project**, rather than a production-ready commercial website.

---

# 4. Main Learning Context

The purpose of this project is not only to produce a visually complete webpage, but also to practice putting several introductory web-development concepts together into one functioning interface.

Instead of treating HTML elements independently, the project combines them into a larger website structure.

For example:

```text
HTML
│
├── Header / Navigation
├── Hero Section
├── Services
├── How It Works
├── Repair Request Form
│   ├── Customer Information
│   ├── Device Information
│   ├── Problem Description
│   ├── Priority
│   ├── Additional Services
│   └── Preferred Date
└── Footer
```

CSS is then used to control how these elements are presented and arranged.

---

# 5. Website Structure

## Header

The header contains:

* TechFix logo
* Navigation links
* "Book a Repair" button

The navigation links use HTML anchor links such as:

```html
<a href="#services">Services</a>
<a href="#process">How It Works</a>
<a href="#booking">Book Repair</a>
<a href="#contact">Contact</a>
```

These allow the user to move to different sections of the same page.

---

## Hero Section

The hero section introduces the purpose of the website.

It contains:

* Business/service description
* Main headline
* Supporting description
* Primary call-to-action
* Secondary call-to-action
* A visual "Technical Diagnostics" card

The diagnostic card is a **visual interface element** and does not perform actual hardware or software diagnostics.

---

# 6. Services Section

The services section presents six service cards:

1. Hardware Repair
2. Software Troubleshooting
3. Malware Removal
4. System Upgrade
5. Data Recovery
6. Not Sure?

Each service card demonstrates the use of structured HTML elements such as:

```html
<article>
<h3>
<p>
<span>
<strong>
<a>
```

CSS Grid is used to arrange the cards.

On larger screens, the cards are displayed in three columns. On smaller screens, the layout changes to fewer columns and eventually a single-column layout.

---

# 7. How It Works Section

The process section explains the fictional repair workflow:

```text
01 — Tell us the problem
02 — We diagnose it
03 — We repair it
04 — We test it
```

This section demonstrates how repeated content can be organized into a consistent visual structure.

---

# 8. Repair Request Form

The booking form is one of the main interactive portions of the website.

It demonstrates several HTML form controls.

## Customer Information

The form asks for:

* Full Name
* Email Address
* Contact Number

Example:

```html
<input
    type="text"
    id="name"
    name="name"
    required
>
```

The `required` attribute provides basic browser-side validation.

---

## Device Information

A `<select>` dropdown is used to select the device type.

Available examples include:

* Laptop
* Desktop PC
* All-in-One PC
* MacBook / iMac
* Mini PC
* Other

A second dropdown is used to select the requested service.

---

## Problem Description

A `<textarea>` allows the customer to describe the problem.

This provides an example of a form field that can accept a longer amount of text compared with a normal `<input>`.

---

# 9. Radio Buttons

The Priority section uses radio buttons:

* Standard
* Urgent
* Emergency

Because the radio buttons use the same `name`:

```html
name="priority"
```

the user can select only one priority.

This demonstrates the purpose of radio-button groups in HTML forms.

---

# 10. Checkboxes

The Additional Services section uses checkboxes.

Available options include:

* Internal Cleaning
* Data Backup
* Software Installation
* Performance Optimization

Unlike radio buttons, checkboxes allow multiple options to be selected.

The form uses:

```html
name="additional_services[]"
```

to represent the possibility of multiple selected services.

---

# 11. Date Input

The form also contains a date input:

```html
<input
    type="date"
    id="date"
    name="date"
    required
>
```

This allows the browser to provide a date-selection interface.

---

# 12. Form Submission

The current form does **not** send information to a real server.

Instead, it uses:

```html
onsubmit="alert('Message Sent successfully! (Simulation only)'); return false;"
```

This means that when the form passes the browser's basic validation, an alert message appears.

`return false` prevents the form from actually being submitted.

Therefore, the current implementation should be considered a:

> **Simulation of a repair-request submission**

rather than a real booking system.

---

# 13. Responsive Design

The website includes CSS media queries to adapt its layout to different screen sizes.

Two main breakpoints are used:

```css
@media (max-width: 900px)
```

and:

```css
@media (max-width: 620px)
```

For example, the service grid changes from three columns on larger screens to two columns on tablet-sized screens and eventually one column on mobile screens.

The booking form also changes from a two-column layout to a single-column layout on smaller devices.

This demonstrates the basic principle of **responsive web design**.

---

# 14. CSS Organization

The CSS file is divided into sections such as:

```text
Variables
Reset
Container
Header
Hero
Buttons
Diagnostic Card
General Section
Services
Process
Booking
Form Card
Priority
Checkboxes
Form Actions
Footer
Tablet
Mobile
```

This organization makes the stylesheet easier to navigate and maintain.

CSS custom properties are also used:

```css
:root {
    --navy: #0b1f33;
    --blue: #1677ff;
    --cyan: #25c7e8;
    --ink: #132536;
    --muted: #667789;
}
```

This allows commonly used colors to be defined in one place and reused throughout the stylesheet.

---

# 15. Design Approach

The visual design uses a technology-oriented style based around:

* Dark navy
* Blue
* Cyan
* White
* Light gray backgrounds

The intention is to give the website a clean and technical appearance appropriate for a computer repair service.

The design also uses:

* Cards
* Rounded corners
* Shadows
* Grid layouts
* Hover effects
* Responsive layouts
* Call-to-action buttons
* Visual hierarchy

These are primarily implemented through CSS.

---

# 16. What Is Actually Functional?

### Currently functional

* Navigation links to page sections
* Responsive layout
* Form controls
* Dropdown selections
* Radio buttons
* Checkboxes
* Date selection
* Basic browser form validation through `required`
* Hover effects
* Simulated form-submission alert

### Currently simulated / not connected to a backend

* Actual repair booking
* Customer database
* Email notification
* Technician assignment
* Real diagnostics
* Real malware scanning
* Real data recovery
* Payment
* Appointment scheduling
* User accounts
* Server-side validation

The service descriptions and prices are also part of the fictional/demo website concept.

---

# 17. Current Limitations

This project is a **front-end educational prototype**.

It does not currently include:

```text
Frontend
   ↓
Backend server
   ↓
Database
   ↓
Actual service/booking system
```

The current implementation effectively ends at the browser.

A future version could connect the form to a backend application and database so that submitted repair requests could actually be stored and processed.

---

# 18. Possible Future Development

If the project were developed further, possible additions could include:

### Backend

* Server-side form processing
* Database storage
* Authentication
* Customer accounts
* Technician accounts

### Booking System

* Real appointment scheduling
* Available time slots
* Technician availability
* Booking confirmation

### Communication

* Email confirmation
* SMS notifications
* Repair-status updates

### Repair Management

```text
Request
   ↓
Diagnosis
   ↓
Quote
   ↓
Customer Approval
   ↓
Repair
   ↓
Testing
   ↓
Completed
```

### Security

* Server-side validation
* Input sanitization
* Authentication
* Authorization
* Secure password handling
* Protection against common web attacks

---

# 19. Important Distinction

This project demonstrates the **interface and structure** of a computer repair service website.

It should not be interpreted as claiming that the website itself can perform computer diagnostics, malware removal, or data recovery.

Those services are represented as the fictional business's offerings, while the website currently serves as their front-end presentation and simulated request interface.

---

# 20. Summary

TechFix is an introductory BSIT front-end project that combines previously encountered HTML and CSS concepts into a larger website.

The project demonstrates practical use of:

**HTML**

→ semantic page structure
→ navigation
→ forms
→ input types
→ radio buttons
→ checkboxes
→ dropdowns
→ textarea
→ buttons
→ labels
→ basic validation

**CSS**

→ external stylesheet
→ variables
→ layouts
→ CSS Grid
→ responsive design
→ media queries
→ visual hierarchy
→ cards
→ hover effects
→ spacing and typography

**Basic JavaScript**

→ simulated form submission using `alert()`

The project represents an early step toward understanding how individual web-development concepts can be combined into a complete user-facing interface.

---

## Submission Note

This project was created for **educational/academic purposes** as an undergraduate BSIT project.

The website's business, services, prices, diagnostics interface, and repair-request system are presented as a demonstration/prototype and are not intended to represent a fully operational commercial repair center.
