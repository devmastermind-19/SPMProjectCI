# QuickPOS ⚡

Modern Point of Sale (POS) Landing Page with Full Stack Integration and CI/CD Pipeline.

## 📋 Project Overview
QuickPOS is a professional, responsive landing page for a POS system. It features a modern, SaaS-style UI built with HTML/CSS/JS and a secure PHP/MySQL backend for contact form handling. Developed using Software Project Management (SPM) best practices including GitFlow, automated testing, and CI/CD.

## 🛠️ Tech Stack
- **Frontend:** HTML5, CSS3 (Custom Design System, Glassmorphism), Vanilla JavaScript
- **Backend:** PHP 8.1+ (PDO)
- **Database:** MySQL
- **Testing:** PHPUnit
- **Static Analysis:** PHPStan
- **CI/CD:** GitHub Actions

## 🚀 Setup Guide

### 1. Prerequisites
- PHP 8.1 or higher
- MySQL / MariaDB
- Composer (for PHPUnit/PHPStan)
- A local web server (XAMPP, MAMP, or PHP Built-in server)

### 2. Database Setup
1. Open your MySQL client (e.g., phpMyAdmin or command line).
2. Create the database:
   ```sql
   CREATE DATABASE quickpos_db;
   ```
3. Create the table:
   ```sql
   USE quickpos_db;

   CREATE TABLE contact_messages (
       id INT AUTO_INCREMENT PRIMARY KEY,
       name VARCHAR(255) NOT NULL,
       email VARCHAR(255) NOT NULL,
       message TEXT NOT NULL,
       created_at DATETIME DEFAULT CURRENT_TIMESTAMP
   );
   ```
4. Configure database credentials in `includes/db.php` if needed (default uses `root` with no password).

### 3. Running Locally
Using PHP's built-in server:
```bash
# Clone the repository
git clone https://github.com/yourusername/quickpos.git
cd quickpos

# Start the server
php -S localhost:8000
```
Visit `http://localhost:8000` in your browser.

## 🧪 Testing

### Setup Dependencies
Install development dependencies (PHPUnit, PHPStan) using Composer:
```bash
composer install
```

### Run Tests
```bash
# Run PHPUnit tests
composer test
# OR
./vendor/bin/phpunit

# Run Static Analysis (PHPStan)
composer analyse
```

## 🌿 Git Workflow (GitFlow)
We strictly follow a structured branching strategy:
- `main`: Production-ready code only.
- `develop`: Active development branch.
- `feature/*`: For new features (e.g., `feature/POS-101-hero-section`).
- `bugfix/*`: For bug fixes.

**Rules:**
- No direct commits to `main`.
- All work is merged via Pull Requests (PRs).
- Mandatory PR reviews.
- Commit format: `[POS-XXX] Brief description of changes`.

## ⚙️ CI/CD Pipeline
Our GitHub Actions pipeline (`.github/workflows/ci.yml`) automates quality assurance:
1. **Checkout:** Pulls the latest code.
2. **Setup PHP:** Configures the PHP environment.
3. **Syntax Check:** Verifies PHP file syntax (`php -l`).
4. **Code Quality:** Runs PHPStan to catch potential bugs.
5. **Testing:** Executes PHPUnit test suite.
6. **PR Blocking:** Pull Requests are blocked from merging if any checks fail.

## 📸 Screenshots

<img width="948" height="437" alt="image" src="https://github.com/user-attachments/assets/4037eaeb-0a02-473a-9e80-8c1f7bddf8c8" />

<img width="947" height="439" alt="image" src="https://github.com/user-attachments/assets/7831e553-8be8-46bc-9b3b-58b93145b6c1" />

<img width="950" height="442" alt="image" src="https://github.com/user-attachments/assets/10e3d79a-c542-4459-9484-f87184ff4b93" />

<img width="952" height="439" alt="image" src="https://github.com/user-attachments/assets/41f9e159-4c9d-4564-ac3b-36b5491dd80b" />

<img width="959" height="391" alt="image" src="https://github.com/user-attachments/assets/c939023b-e614-460e-91b2-690fa7914ee7" />

<img width="947" height="446" alt="image" src="https://github.com/user-attachments/assets/73fc1c03-1d17-4800-bb55-38f949cd3ee7" />


*Developed for SPM Semester Project.*
