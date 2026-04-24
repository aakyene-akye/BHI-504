# 💊 Secure Prescription Reminder App with Safety Features

> A Python-based prescription reminder application with drug interaction checking and safety features for improved medication adherence.

**Course:** BHI 507 - Biomedical and Health Informatics  
**Institution:** SUNY Oswego  
**Semester:** Spring 2025

---

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Code Structure](#code-structure)
- [Testing](#testing)
- [Project Highlights](#project-highlights)

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
- Python 3.8 or higher

### Steps

1. **Clone the repository:**
```bash
   git clone https://github.com/aakyene-akye/secure-prescription-reminder-app.git
   cd secure-prescription-reminder-app
```

2. **No additional installation needed!**
   The project uses only Python standard library.

3. **Verify Python version:**
```bash
   python3 --version
```
   Should output Python 3.8 or higher.

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

## 🧪 Testing

The project includes **comprehensive test coverage** to ensure reliability:

### Test Categories

| Test Type | Coverage | Test Count |
|-----------|----------|------------|
| User Authentication | Login/logout, password validation | 5 tests |
| Prescription Management | Create, track, retrieve prescriptions | 4 tests |
| Drug Interaction Checker | Detect interactions, handle edge cases | 3 tests |
| Reminder Service | Send reminders, track history | 3 tests |
| Integration Testing | Complete user workflows | 1 test |

## 🌟 Project Highlights

### Health Informatics Concepts Demonstrated

1. **Patient Safety**
   - Drug interaction checking reduces adverse events
   - Automated reminders improve adherence
   - Data validation prevents errors

2. **Clinical Decision Support**
   - Real-time interaction alerts
   - Evidence-based warnings
   - Actionable recommendations

3. **Health Data Management**
   - Structured data storage
   - CRUD operations (Create, Read, Update, Delete)
   - Data integrity through validation

4. **User-Centered Design**
   - Simple authentication flow
   - Clear error messages
   - Intuitive class structure


