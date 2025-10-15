# Online Health Prediction Platform

## Video Demonstration

Watch the complete walkthrough of the platform's features:

- **Full Project Demo**: https://www.loom.com/share/65c98de8e06c47dc83226da3cb9c0542?sid=35e23e56-dc53-4fde-9036-4e396afe8a02


## Overview

I developed a comprehensive Django-based web application that leverages machine learning to provide health condition predictions. The platform analyzes user-provided data to predict potential risks for mental health disorders, PCOS (Polycystic Ovary Syndrome), and obesity using trained ML models. Beyond predictions, the system facilitates complete healthcare management including report generation, appointment scheduling, and doctor-patient communication.

**⚠️ DISCLAIMER**: This project is developed solely for educational and demonstration purposes. The predictions are not medically accurate and should never be used for actual medical diagnosis or treatment decisions. Always consult qualified healthcare professionals for medical advice.

## Key Features

### For Patients
- **AI-Powered Health Predictions**: Generate instant predictions for mental health conditions, PCOS, and obesity risk levels
- **Downloadable Health Reports**: Export comprehensive PDF reports containing prediction results and health insights
- **Appointment Booking System**: Schedule consultations with registered healthcare providers through an intuitive interface
- **User Dashboard**: Track medical history, view past predictions, and manage appointments from a centralized dashboard
- **Secure Registration & Authentication**: Protected user accounts with personal health data privacy

### For Healthcare Providers
- **Doctor Registration Portal**: Healthcare professionals can create verified accounts on the platform
- **Appointment Management**: View, accept, or decline appointment requests from patients
- **Patient Communication**: Direct messaging system for coordinating consultations and follow-ups
- **Request Queue**: Organized interface to manage multiple appointment requests efficiently

## Technology Stack

**Frontend**
- HTML5
- CSS3
- Bootstrap Framework

**Backend**
- Python 3.x
- Django 5.0.2
- SQLite3 Database

**Machine Learning**
- Scikit-learn
- Pandas & NumPy
- Pre-trained classification models

## Installation & Setup

### Prerequisites
- Python 3.8 or higher
- pip package manager

### Step 1: Clone the Repository
```bash
git clone https://github.com/dev52003/PredictCare.git
cd PredictCare/
```

### Step 2: Install Dependencies
```bash
pip install -r requirements.txt
```

If any specific package is missing, install it manually:
```bash
pip install <package-name>
```

### Step 3: Database Configuration
Run migrations to set up the database schema:
```bash
python manage.py makemigrations
python manage.py migrate
```

### Step 4: Launch the Application
Start the Django development server:
```bash
python manage.py runserver
```

### Step 5: Access the Platform
Open your web browser and navigate to:
```
http://127.0.0.1:8000/
```

## Project Architecture

```
predictHealth/                 # Root directory
│
├── manage.py                  # Django management script
├── requirements.txt           # Python dependencies
│
├── home/                      # Main Django application
│   ├── models.py             # Database models
│   ├── views.py              # Business logic and controllers
│   ├── urls.py               # URL routing
│   └── forms.py              # Form definitions
│
├── static/                    # Static assets
│   ├── css/                  # Stylesheets
│   ├── images/               # Image files
│   ├── datasets/             # Training datasets (CSV files)
│   ├── encoders/             # Preprocessing encoders
│   └── ml_models/            # Saved ML prediction models
│
└── templates/                 # HTML templates
    ├── base.html             # Base template
    ├── home.html             # Landing page
    ├── login.html            # Authentication
    └── dashboard.html        # User interfaces
```

## Machine Learning Models

The platform utilizes three distinct prediction models, each trained on curated datasets:

1. **Mental Health Disorder Classifier**: Predicts likelihood of various mental health conditions based on behavioral and psychological indicators
2. **PCOS Risk Predictor**: Analyzes hormonal and physiological markers to assess PCOS probability
3. **Obesity Classification Model**: Evaluates lifestyle factors, dietary habits, and physical measurements to classify obesity risk

All models were trained using datasets sourced from Kaggle and employ various classification algorithms optimized for healthcare prediction tasks.

## Data Sources

The machine learning models were trained using the following publicly available datasets:

- **Obesity Prediction Dataset**: [Kaggle Obesity Data](https://www.kaggle.com/datasets/mrsimple07/obesity-prediction)
- **Mental Disorder Classification Dataset**: [Kaggle Mental Health Data](https://www.kaggle.com/datasets/cid007/mental-disorder-classification)
- **PCOS Diagnostic Dataset**: [Kaggle PCOS 2023 Dataset](https://www.kaggle.com/datasets/sahilkoli04/pcos2023)

---

**Remember**: This is a prototype system designed to demonstrate the integration of machine learning with web applications. Never use this platform for actual medical decision-making. Always seek professional medical advice for health concerns.