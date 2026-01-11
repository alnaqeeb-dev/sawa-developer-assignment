# MedBook - Developer Technical Assignment

## Overview

Build an **Appointment Booking** platform for a medical clinic. The platform connects **Patients** who want to book appointments with **Doctors** who manage their schedules.

---

## Product Context

**MedBook** is a platform where:

- **Patients** browse doctors and book appointments
- **Doctors** manage their appointments and respond to booking requests

### User Flow

**Patient:**

1. Browse available doctors
2. Filter by specialty
3. View doctor details (bio, experience, fees, availability)
4. Book an appointment
5. See appointment status (pending/confirmed/rejected)

**Doctor:**

1. View appointment requests
2. Confirm or reject appointments

---

## Tech Stack

- **Frontend:** React (TypeScript)
- **Backend:** Node.js with Express (TypeScript)

You are free to use any additional libraries, state management, styling approach, or tools you prefer.

---

## Requirements

### Part 1: Patient Frontend

#### 1.1 Doctor List Page (`/`)

- [ ] Fetch and display doctors from the backend API
- [ ] Display: name, specialty, hospital, rating, fee
- [ ] Add specialty filter (general, cardiology, dermatology, pediatrics, orthopedics)
- [ ] Handle loading and error states

#### 1.2 Doctor Detail Page (`/doctors/:id`)

- [ ] Fetch and display doctor details
- [ ] Show: bio, experience, available days, location, fee
- [ ] Include appointment booking form or button

#### 1.3 Appointment Booking Form

- [ ] Fields: patient name, email, phone, date, time, reason for visit
- [ ] Submit appointment to the backend API
- [ ] New appointments start with status "pending"
- [ ] Show feedback on success/failure

---

### Part 2: Doctor Frontend

#### 2.1 Doctor Dashboard (`/doctor/:doctorId`)

- [ ] Display list of appointments for this doctor
- [ ] Show: patient name, date, time, reason, status
- [ ] Provide buttons to Confirm or Reject pending appointments

---

### Part 3: Backend API

#### Endpoints

| Method | Endpoint                              | Description                                    |
| ------ | ------------------------------------- | ---------------------------------------------- |
| GET    | `/api/doctors`                        | List all doctors. Support `?specialty=` filter |
| GET    | `/api/doctors/:id`                    | Get single doctor by ID                        |
| POST   | `/api/appointments`                   | Create a new appointment (status: pending)     |
| GET    | `/api/doctors/:doctorId/appointments` | Get all appointments for a doctor              |
| PATCH  | `/api/appointments/:id/confirm`       | Confirm an appointment                         |
| PATCH  | `/api/appointments/:id/reject`        | Reject an appointment                          |

## Getting Started

### 1. Install Dependencies

```bash
npm install
```

### 2. Start Development Servers

```bash
npm run start
```

### 3. Access the App

- Frontend: http://localhost:5173
- Backend API: http://localhost:3001

---

## Project Structure

```
sawa-developer-assignment/
├── src/                  # Frontend (React)
│   ├── App.tsx
│   ├── main.tsx
│   ├── types/index.ts    # TypeScript types
│   └── ...               # Add your own structure
├── server/
│   ├── index.ts          # Express server (starter)
│   └── data.ts           # Sample data (provided)
├── package.json
└── README.md
```

---

## Sample Data

**Doctors:** 10 doctors across 5 specialties

- Specialties: general, cardiology, dermatology, pediatrics, orthopedics

**Appointments:** 4 sample appointments

- 3 pending, 1 confirmed

See `server/data.ts` for full data.

---

## What We Provide

- Basic React + Vite + TypeScript setup
- Express server starter
- TypeScript types for Doctor, Appointment
- Sample data (10 doctors, 4 appointments)

---

## What You Build

- Patient: Doctor list, detail page, booking form
- Doctor: Dashboard to confirm/reject appointments
- Backend: 6 API endpoints
- Your choice of styling and state management

## Questions?

If something is unclear, make a reasonable assumption and document it in NOTES.md.

Good luck!
# sawa-developer-assignment
