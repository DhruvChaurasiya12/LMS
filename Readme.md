# Loan Management System (LMS)

## Overview

Loan Management System (LMS) is a role-based web application that automates the complete loan lifecycle, from borrower registration and loan application to sanction, disbursement, repayment collection, and loan closure.

The system implements a multi-role workflow with secure authentication, authorization, Business Rule Engine (BRE) validation, and dashboard analytics.

---

## Features

### Authentication & Authorization

* JWT-based Authentication
* Password Hashing using bcrypt
* Role-Based Access Control (RBAC)
* Protected Routes
* Secure Login & Registration

### Roles

#### Borrower

* Register/Login
* Apply for Loan
* Upload Salary Slip
* View Loan History
* View Loan Status
* Change Password

#### Sales

* View registered borrowers who have not applied for loans

#### Sanction

* Review loan applications
* Approve loan applications
* Reject loan applications with reason

#### Disbursement

* View sanctioned loans
* Mark loans as disbursed

#### Collection

* Record repayments
* UTR validation
* View outstanding balances
* Auto-close fully repaid loans

#### Admin

* Access all modules
* Dashboard Analytics
* Create Employee Accounts
* Manage Sales, Sanction, Disbursement, and Collection users

---

## Business Rule Engine (BRE)

Loan applications are validated using the following rules:

### Age Validation

* Minimum Age: 23 Years
* Maximum Age: 50 Years

### Salary Validation

* Monthly Salary ≥ ₹25,000

### Employment Validation

* Employment Status cannot be UNEMPLOYED

### PAN Validation

Valid PAN Format:

ABCDE1234F

### Salary Slip

Salary Slip upload is mandatory.

---

## Loan Workflow

Borrower Registration
↓
Loan Application
↓
Sales Review
↓
Sanction Approval / Rejection
↓
Disbursement
↓
Collection
↓
Loan Closure

---

## Interest Calculation

Interest Formula:

Interest = (Loan Amount × 12 × Tenure) / (365 × 100)

Total Repayment:

Total Repayment = Principal + Interest

---

## Dashboard Features

* Total Loans
* Applied Loans
* Sanctioned Loans
* Disbursed Loans
* Closed Loans
* Rejected Loans

### Visualizations

* Pie Chart
* Bar Chart

---

## Tech Stack

### Frontend

* Next.js 16
* TypeScript
* Tailwind CSS
* Axios
* Recharts

### Backend

* Node.js
* Express.js
* TypeScript
* MongoDB
* Mongoose

### Authentication

* JWT
* bcryptjs

### File Upload

* Multer

---

## Project Structure

backend/
├── src/
│ ├── controllers/
│ ├── routes/
│ ├── middleware/
│ ├── models/
│ ├── config/
│ └── server.ts

frontend/
├── src/
│ ├── app/
│ ├── components/
│ ├── lib/

---

## Environment Variables

### Backend (.env)

PORT=5000

MONGO_URI=your_mongodb_connection_string

JWT_SECRET=your_secret_key

### Frontend (.env)

NEXT_PUBLIC_API_URL=http://localhost:5000/api

---

## Installation

### Clone Repository

git clone <repository-url>

cd LMS

---

## Backend Setup

cd backend

npm install

### Start Backend

npm run dev

---

## Frontend Setup

cd frontend

npm install

### Start Frontend

npm run dev

---

## Seed Data

Run:

npm run seed

This creates the default users below.

---

## Demo Credentials

### Admin

Email: [admin@test.com](mailto:admin@test.com)

Password: 123456

### Sales

Email: [sales@test.com](mailto:sales@test.com)

Password: 123456

### Sanction

Email: [sanction@test.com](mailto:sanction@test.com)

Password: 123456

### Disbursement

Email: [disbursement@test.com](mailto:disbursement@test.com)

Password: 123456

### Collection

Email: [collection@test.com](mailto:collection@test.com)

Password: 123456

### Borrower

Email: [borrower@test.com](mailto:borrower@test.com)

Password: 123456

---

## Security Features

* Password Hashing
* JWT Authentication
* Role-Based Access Control
* Protected APIs
* Protected Frontend Routes
* Duplicate UTR Prevention
* Loan Eligibility Validation

---

## Future Enhancements

* Email Notifications
* OTP Verification
* Loan EMI Schedule
* Profile Photo Upload
* Audit Logs
* Loan Document Management
* Advanced Analytics Dashboard

---

## Author

Developed as part of an LMS Assignment Submission using Next.js, TypeScript, Express.js, and MongoDB.
