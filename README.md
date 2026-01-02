# 🚀 CareerHub - Advanced Job Portal System

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python)
![Django](https://img.shields.io/badge/Django-4.2%2B-092E20?style=for-the-badge&logo=django)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Active-success?style=for-the-badge)

> **A comprehensive recruitment platform bridging the gap between talent and opportunity through secure, role-based interaction.**



## 📋 Overview

**CareerHub** is a full-stack Django application designed to streamline the recruitment process. It features a robust **Role-Based Access Control (RBAC)** system that creates distinct, secure environments for Administrators, Job Providers (Recruiters), and Job Seekers (Candidates). 

This project demonstrates advanced database modeling, secure authentication, and complex workflow management using Python and Django.

---

## 👥 Architecture: Role-Based Access Control

The system separates functionality into three distinct tiers to ensure data security and workflow efficiency.

| Role | Access Level | Primary Responsibilities |
| :--- | :--- | :--- |
| **👑 Admin** | **Superuser** | System monitoring, user management, content moderation, analytics. |
| **💼 Job Provider** | **Recruiter** | Post vacancies, screen applications, download resumes, schedule interviews. |
| **👨‍💻 Job Seeker** | **Candidate** | Build profile, search jobs, apply with one click, track application status. |

---

## ✨ Key Features

### 🏢 For Job Providers (Recruiters)
* **Vacancy Management:** Create, edit, and close job listings with rich text descriptions.
* **Application Tracking:** View list of applicants for specific posts.
* **Resume Screening:** Direct access to candidate resumes and profiles.
* **Company Profile:** Manage company branding and details.

### 👨‍🎓 For Job Seekers (Candidates)
* **Advanced Search:** Filter jobs by category, location, and salary.
* **Smart Profile:** Upload resume/CV, add skills, and work experience.
* **Application History:** Track the status of applied jobs (Pending, Accepted, Rejected).
* **Alerts:** (Optional) Notifications for relevant job openings.

### ⚙️ Core System Features
* **Secure Authentication:** Login/Signup with Django Auth.
* **Responsive Design:** optimized for mobile and desktop viewing.
* **Dynamic Filtering:** Real-time job search capabilities.

---

## 🛠️ Tech Stack

| Domain | Technologies Used |
| :--- | :--- |
| **Backend** | Python 3.8+, Django 4.2+ |
| **Frontend** | HTML5, CSS3 (Bootstrap/Tailwind), JavaScript |
| **Database** | SQLite (Dev) / PostgreSQL (Production) |
| **Security** | Django Role-Based Access, CSRF Protection |

---

## 🚀 Quick Start Guide

### Prerequisites
* Python 3.8+
* pip

### Installation

1.  **Clone the repository**
    ```bash
    git clone [https://github.com/your-username/careerhub.git](https://github.com/your-username/careerhub.git)
    cd careerhub
    ```

2.  **Set up Virtual Environment**
    ```bash
    # Windows
    python -m venv venv
    venv\Scripts\activate
    
    # macOS/Linux
    python3 -m venv venv
    source venv/bin/activate
    ```

3.  **Install Dependencies**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Run Migrations**
    ```bash
    python manage.py makemigrations
    python manage.py migrate
    ```

5.  **Create Admin User**
    ```bash
    python manage.py createsuperuser
    ```

6.  **Run Server**
    ```bash
    python manage.py runserver
    ```
    Visit `http://localhost:8000`

---


🎮 Usage Guide
1. Setting up the Master Admin
Log in via /admin.

Verify new company registrations.

Manage job categories (e.g., "IT", "Marketing", "Finance").

2. Posting a Job (Provider)
Register as a "Recruiter".

Navigate to Dashboard > Post New Job.

Fill in details (Title, Salary, Description) and Publish.

3. Applying for a Job (Seeker)
Register as a "Job Seeker".

Complete your profile (Upload Resume).

Browse the Home Page and click "Apply Now" on any listing.

🛡️ Security & Best Practices
Password Hashing: Uses Django’s PBKDF2 password hasher.

Permissions: Decorators like @login_required and custom @recruiter_required ensure strict access control.

Data Protection: CSRF tokens on all forms to prevent cross-site attacks.

📞 Contact & Author
Arpit Bhojani - Python Developer

📧 Email: bhojaniarpit1432@gmail.com

📱 Phone: +91 7383181094

<div align="center"> <sub>Built with ❤️ and Django.</sub> </div>

## 📂 Project Structure

<details>
<summary>Click to expand file tree</summary>

```text
careerhub/
├── accounts/            # User Authentication & Role Management
│   ├── models.py        # Custom User Model (AbstractUser)
│   ├── views.py         # Login/Signup Logic
│   └── templates/       # Auth Forms
├── jobs/                # Job Posting & Application Logic
│   ├── models.py        # Job, Application, Category Models
│   ├── views.py         # CRUD operations for Jobs
│   └── templates/       # Job Lists & Details
├── careerhub/           # Project Settings
│   ├── settings.py
│   └── urls.py
├── static/              # CSS, JS, Images
├── media/               # User Resumes & Profile Pics
├── manage.py
└── requirements.txt
