# Nagara Netra

### AI-Powered Multimodal Civic Grievance Management System

Nagara Netra is an AI-powered civic grievance management platform that helps citizens report issues such as roads, drainage, garbage, water, streetlights, electricity, safety, and traffic problems.

Citizens can submit complaints using **images, voice, or text**. The system uses AI to understand the complaint, identify the issue, predict the responsible department and priority, generate structured complaint information, and route the complaint to the appropriate officer.

## Key Features

* Multimodal complaint submission using image, voice, and text
* Civic issue classification using EfficientNet-B0
* Image analysis and description using BLIP
* Multilingual text processing using MuRIL
* Voice-to-text processing using OpenAI Whisper
* AI-assisted complaint analysis using LLMs
* Automatic department and priority prediction
* Location selection using an interactive map
* Role-based access for Citizens, Officers, and Admins
* Officer assignment and complaint tracking
* Complaint status management
* Real-time notifications using WebSockets
* Admin dashboard with analytics and complaint management
* SLA monitoring and escalation alerts
* Image compression and API rate limiting

## System Workflow

```text
Image / Voice / Text
        ↓
Input Processing
        ↓
AI Analysis
        ↓
Issue Detection
        ↓
Department Prediction
        ↓
Priority Prediction
        ↓
Location Selection
        ↓
Complaint Generation
        ↓
Officer Assignment
        ↓
Status Tracking
        ↓
Resolution
```

## Technology Stack

### Frontend

* Next.js
* React
* TypeScript
* Tailwind CSS
* React Three Fiber / Three.js
* Recharts

### Backend

* Python
* FastAPI
* REST APIs
* WebSockets
* SQLAlchemy

### AI/ML

* PyTorch
* EfficientNet-B0
* BLIP
* MuRIL
* OpenAI Whisper
* LLM-based processing

### Database and Cloud

* PostgreSQL
* Amazon S3
* Amazon DynamoDB
* Amazon SNS
* Amazon Bedrock
* AWS IAM

### Security

* JWT Authentication
* Role-Based Access Control
* Password Hashing
* API Rate Limiting

## User Roles

### Citizen

* Register and submit complaints
* Upload images or record voice complaints
* Select complaint location
* Track complaint status
* Receive notifications

### Officer

* View assigned complaints
* Update complaint status
* Manage complaint resolution
* Receive assignment notifications

### Admin

* Manage users and departments
* Monitor complaints
* View analytics
* Monitor SLA compliance
* Manage complaint assignments

## Project Structure

```text
Nagara_Netra/
├── frontend/
│   ├── src/
│   │   ├── app/
│   │   ├── components/
│   │   ├── auth/
│   │   └── hooks/
│   └── package.json
│
├── backend/
│   ├── app/
│   │   ├── ai/
│   │   ├── auth/
│   │   ├── core/
│   │   ├── database/
│   │   ├── routers/
│   │   └── main.py
│   ├── scripts/
│   └── requirements.txt
│
└── README.md
```

## Running Locally

### Frontend

```bash
cd frontend
npm install
npm run dev
```

Frontend:

```text
http://localhost:3000
```

### Backend

```bash
cd backend
python -m venv venv
```

Windows:

```bash
venv\Scripts\activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Configure the required environment variables in `.env`, then start the server:

```bash
python -m uvicorn app:app --reload
```

Backend:

```text
http://localhost:8000
```

API documentation:

```text
http://localhost:8000/docs
```

## Deployment

The application is designed to be deployed using AWS services.

```text
Users
  ↓
EC2
  ├── Next.js Frontend
  └── FastAPI Backend
          ↓
      RDS PostgreSQL
          ↓
   AWS Services
   ├── S3
   ├── DynamoDB
   ├── SNS
   └── Bedrock
```

## Project Objective

The objective of Nagara Netra is to simplify civic complaint reporting and assist municipal teams by using AI for complaint understanding, classification, prioritization, and routing.


