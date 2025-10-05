# 🏥 MediCare - Healthcare Management API

A modern, secure REST API for managing healthcare operations, built with Django. Perfect for clinics and healthcare providers who need to manage patients, doctors, and appointments efficiently.

![Python Version](https://img.shields.io/badge/Python-3.11+-blue)
![Django Version](https://img.shields.io/badge/Django-5.0.1-green)
![PostgreSQL](https://img.shields.io/badge/Database-PostgreSQL-blue)

## ✨ What Can You Do With This?

### 👥 For Patients
- Create and manage patient profiles
- Book appointments with doctors
- View medical history
- Track appointments and status

### 👨‍⚕️ For Doctors
- Manage professional profiles
- Track patient assignments
- Handle appointment schedules
- Update patient records

### 📊 For Administrators
- Manage user accounts
- Handle doctor-patient relationships
- Monitor system activity
- Generate reports

## 🚀 Quick Start Guide

### 1. Get Your System Ready
Make sure you have:
- Python 3.11 or newer
- PostgreSQL database
- pip package manager

### 2. Set Up Your Project

```bash
# Clone and move into the project
git clone <your-repo-url>
cd medicare

# Create your virtual environment
python -m venv venv

# Activate it (Windows)
venv\Scripts\activate

# Install what you need
pip install -r requirements.txt
```

### 3. Configure Your Environment

Create a `.env` file with:
```env
DEBUG=True
SECRET_KEY=your-secret-key
DB_NAME=your_db_name
DB_USER=your_db_user
DB_PASSWORD=your_password
DB_HOST=localhost
DB_PORT=5432
```

### 4. Get the Database Ready

```bash
python manage.py makemigrations
python manage.py migrate
python manage.py createsuperuser
```

### 5. Start the Server

```bash
python manage.py runserver
```

## 🔌 API Endpoints

### Authentication
```http
POST /api/auth/register/  # Register new user
{
    "username": "user1",
    "email": "user1@example.com",
    "password": "secure_password"
}

POST /api/auth/login/     # Get access token
{
    "username": "user1",
    "password": "secure_password"
}
```

### Patient Management
```http
GET    /api/patients/     # List patients
POST   /api/patients/     # Add patient
GET    /api/patients/1/   # View patient
PUT    /api/patients/1/   # Update patient
DELETE /api/patients/1/   # Remove patient
```

### Doctor Management
```http
GET    /api/doctors/      # List doctors
POST   /api/doctors/      # Add doctor
GET    /api/doctors/1/    # View doctor
PUT    /api/doctors/1/    # Update doctor
DELETE /api/doctors/1/    # Remove doctor
```

### Patient-Doctor Mappings
```http
GET    /api/mappings/     # List mappings
POST   /api/mappings/     # Create mapping
DELETE /api/mappings/1/   # Remove mapping
```

## 🔒 Security Features

- JWT-based authentication
- Password hashing & salting
- Role-based access control
- Input validation
- CSRF protection
- Rate limiting

## 🧪 Testing

Run tests with:
```bash
python manage.py test
```

## 📝 Code Quality

We follow:
- PEP 8 style guide
- Django best practices
- Type hinting
- Comprehensive documentation
- Clean code principles

## 🛠️ Technology Stack

- **Backend:** Django 5.0.1
- **API:** Django REST Framework 3.14.0
- **Database:** PostgreSQL
- **Auth:** JWT (djangorestframework-simplejwt)
- **Config:** python-dotenv

## 🤝 Need Help?

1. Check our Issues page
2. Read the Documentation
3. Contact: bhavithapallapu@gmail.com

## 📜 License

MIT License - Feel free to use this for your projects!

## 👏 Acknowledgments

- Django community
- PostgreSQL team
- Open source contributors
