# 💊 Secure Prescription Reminder App with Safety Features

> A Python-based prescription reminder application with drug interaction checking and safety features for improved medication adherence.

**Course:** BHI 504 - Systems Design, Integration, Safety & Security  
**Institution:** SUNY Oswego  
**Semester:** Spring 2026

---

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Code Structure](#code-structure)

---

## 🎯 Overview

This project addresses a critical challenge in healthcare: **medication non-adherence**. Studies show that nearly 50% of patients don't take medications as prescribed, leading to poor health outcomes and increased healthcare costs.

The Secure Prescription Reminder App provides a solution by:
- Helping patients track their medications
- Sending timely reminders
- Checking for dangerous drug interactions
- Maintaining secure patient data

This application demonstrates key health informatics concepts including patient safety, clinical decision support, and secure health data management.

---

## ✨ Features

### 🔐 User Authentication
- Secure login and logout system
- Password validation (minimum 8 characters)
- Session management

### 💊 Prescription Management
- Add and track multiple medications
- Store dosage and frequency information
- Monitor medication adherence (doses taken)
- View detailed prescription information

### ⚠️ Drug Interaction Checker
- Real-time interaction detection
- Database of known drug-drug interactions
- Severity warnings for patient safety
- Common interactions included:
  - Warfarin + Aspirin (bleeding risk)
  - Lisinopril + Ibuprofen (reduced effectiveness)
  - Metformin + Alcohol (lactic acidosis risk)

### ⏰ Reminder System
- Automated medication reminders
- User-specific notifications
- Reminder history tracking
- Timestamp for each reminder

---

## 📥 Installation

### Prerequisites
- You need Python 3.8 or higher

---

## 🚀 Usage

### Running the Application

**Option 1: Using Jupyter Notebook**
```bash
jupyter notebook Secure_Prescription_App.ipynb
```

**Option 2: Using Google Colab**
1. Go to https://colab.research.google.com
2. Upload `Secure_Prescription_App.ipynb`
3. Run all cells

### Quick Start Example

```python
# Create a patient
patient = User("P001", "John Doe", "john@email.com")

# Set password
patient.set_password("Secure123")

# Login
patient.login("Secure123")

# Add a prescription
rx = Prescription("Metformin", "500mg", "twice daily", datetime.date.today())

# Check for drug interactions
checker = DrugChecker()
has_interaction, message = checker.check_interaction("Metformin", "Lisinopril")

# Send reminder
reminder_service = ReminderService()
reminder_service.send_reminder(patient, rx)

# Mark medication as taken
rx.take_medication()
```

---

## 📁 Code Structure

The project consists of **4 main classes** following object-oriented programming principles:

### 1. `User` Class
**Purpose:** Manages patient accounts and authentication

**Attributes:**
- `user_id` - Unique identifier
- `name` - Patient name
- `email` - Contact email
- `password` - Encrypted password storage
- `is_logged_in` - Session status

**Methods:**
- `set_password()` - Set and validate password
- `login()` - Authenticate user
- `logout()` - End session

### 2. `Prescription` Class
**Purpose:** Stores medication information

**Attributes:**
- `medication_name` - Drug name
- `dosage` - Amount per dose
- `frequency` - How often to take
- `start_date` - When prescription begins
- `times_taken` - Adherence tracking

**Methods:**
- `take_medication()` - Record dose taken
- `get_details()` - Retrieve prescription info

### 3. `DrugChecker` Class
**Purpose:** Detects dangerous drug interactions

**Attributes:**
- `interactions` - Database of known interactions

**Methods:**
- `check_interaction()` - Check two medications for conflicts

### 4. `ReminderService` Class
**Purpose:** Send medication reminders to patients

**Attributes:**
- `reminders` - History of sent reminders

**Methods:**
- `send_reminder()` - Create and send reminder
- `get_reminder_count()` - Track total reminders

---




