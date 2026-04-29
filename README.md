# CareerHub - Advanced Job Portal System

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python)
![Django](https://img.shields.io/badge/Django-4.2%2B-092E20?style=for-the-badge&logo=django)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Ready_to_Commit-success?style=for-the-badge)

> **A comprehensive recruitment platform bridging the gap between talent and opportunity through secure, role-based interaction.**

---

## Project Architecture

```text
                                +-------------------+
                                |   Web Browser     |
                                | (Bootstrap/JS)    |
                                +---------+---------+
                                          | (HTTPS)
                                          v
                                +---------+---------+
                                |  Django Framework |
                                | (Logic & Routing) |
                                +----+----+----+----+
                                     |    |    |
              +----------------------+    |    +----------------------+
              |                           |                           |
    +---------v---------+       +---------v---------+       +---------v---------+
    |   Accounts App    |       |    JobsApp        |       |   Admin Dashboard |
    | (Auth & Profiles) |       | (Postings/Apps)   |       | (Management)      |
    +---------+---------+       +---------+---------+       +---------+---------+
              |                           |                           |
              +-------------+-------------+-------------+-------------+
                            |
                            v
                  +---------+---------+
                  |    Database       |
                  | (SQLite/Postgres) |
                  +-------------------+
```

---

## Overview

**CareerHub** is a high-performance Django application designed to streamline the recruitment lifecycle. It utilizes a **Role-Based Access Control (RBAC)** system to provide specialized interfaces for Administrators, Recruiters (Job Providers), and Candidates (Job Seekers).

### User Roles
| Role | Access Level | Responsibilities |
| :--- | :--- | :--- |
| **Admin** | Superuser | Full system control, user moderation, and analytics. |
| **Provider**| Recruiter | Post vacancies, review applications, and manage hiring status. |
| **Seeker**  | Candidate | Build profile, upload resume, search and apply for jobs. |

---

## Screenshots

<div align="center">
  <img src="screenshots/one.png" width="80%" alt="Homepage Overview">
  <p><i>Home Page with Advanced Search</i></p>
  <br>
  <img src="screenshots/two.png" width="80%" alt="Dashboard">
  <p><i>Role-Based Dashboard for Recruiters</i></p>
  <br>
  <img src="screenshots/three.png" width="80%" alt="Job Listings">
  <p><i>Detailed Job Listings & Application View</i></p>
</div>

---

## Key Features

### For Job Providers
*   **Vacancy Management:** Create, update, and close job postings.
*   **Applicant Tracking:** View and filter candidates who applied for specific roles.
*   **Company Branding:** Manage company profile and details.

### For Job Seekers
*   **Smart Search:** Filter by position, location, and job type.
*   **One-Click Apply:** Seamless application process.
*   **Application History:** Track status (Pending/Accepted/Rejected) in real-time.

---

## Test Cases & Validation

| Module | Test Case | Expected Result |
| :--- | :--- | :--- |
| **Auth** | Register with existing email | System returns "Email already exists" error. |
| **Jobs** | Post job without salary | Form fails validation (Salary is required). |
| **Search** | Search for "Python" in "New York" | Returns only relevant job listings. |
| **Access** | Seeker tries to access Admin panel | Redirects to login with Permission Denied. |
| **Apply** | Apply twice for same job | Error message: "You already applied for this job." |

---

## Installation & Setup

### Prerequisites
*   Python 3.8+
*   pip (Python Package Manager)

### Quick Start
1.  **Clone & Enter**
    ```bash
    git clone https://github.com/your-username/CareerHub.git
    cd CareerHub
    ```
2.  **Environment & Dependencies**
    ```bash
    python3 -m venv venv
    source venv/bin/activate
    pip install -r requirements.txt
    ```
3.  **Database Setup**
    ```bash
    python manage.py makemigrations
    python manage.py migrate
    ```
4.  **Launch**
    ```bash
    python manage.py createsuperuser
    python manage.py runserver
    ```

---

## Project Structure
```text
CareerHub/
├── accounts/          # User authentication & Profile management
├── jobs/              # Core project settings
├── jobsapp/           # Job listings, search, & applications
├── screenshots/       # Documentation assets
├── static/            # CSS, JS, and Images
├── templates/         # HTML structure
└── manage.py          # Django entry point
```

---

<div align="center">
  <sub>Built with Python and Django</sub><br>
  <sub>CareerHub - Bridging Talent and Opportunity</sub>
</div>
