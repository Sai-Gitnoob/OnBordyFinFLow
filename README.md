# OnBordyFinFLow
## The file structure
```text
bank-onboarding-system
│
├── backend
│   │
│   ├── controllers
│   │   ├── authController
│   │   ├── eligibilityController
│   │   ├── onboardingController
│   │   ├── ekycController
│   │   └── adminController
│   │
│   ├── routes
│   │   ├── authRoutes
│   │   ├── eligibilityRoutes
│   │   ├── onboardingRoutes
│   │   ├── ekycRoutes
│   │   └── adminRoutes
│   │
│   ├── models
│   │   ├── userModel
│   │   ├── applicationModel
│   │   ├── ekycModel
│   │   └── auditModel
│   │
│   ├── services
│   │   ├── ocrService
│   │   ├── faceVerificationService
│   │   ├── riskScoringService
│   │
│   ├── middleware
│   │   ├── authMiddleware
│   │   └── roleMiddleware
│   │
│   ├── sockets
│   │   └── socketServer
│   │
│   ├── config
│   │   └── database
│   │
│   └── server.js
│
│
├── frontend
│   │
│   ├── public
│   │
│   ├── src
│   │   │
│   │   ├── components
│   │   │   ├── forms
│   │   │   ├── dashboard
│   │   │   └── chatbot
│   │   │
│   │   ├── pages
│   │   │   ├── login
│   │   │   ├── register
│   │   │   ├── eligibility
│   │   │   ├── onboarding
│   │   │   ├── dashboard
│   │   │   └── admin
│   │   │
│   │   ├── services
│   │   │   └── apiClient
│   │   │
│   │   ├── hooks
│   │   │
│   │   ├── utils
│   │   │
│   │   └── styles
│   │
│   └── package.json
│
│
├── database
│   ├── schema.sql
│   └── migrations
│
│
├── docs
│   ├── PRD
│   ├── system-design
│   ├── API-docs
│   ├── database-design
│   └── security
│
│
├── .env
├── README.md
└── package.json 
```
---
The very similar project structure is not necessary we will work around some tweaks 
Just the 3 main aspects would be 
- The front end
- The backend 
- The database
```
Frontend (Web App)
       │
       ▼
Backend API
       │
       ▼
Database
```
---


The stack we are gonna use is 

```
Frontend

Use:

Next.js

TypeScript

Tailwind CSS

Why:

Best for forms and dashboards

Easy routing

Clean UI

Backend

Use:

Node.js

Express.js

Socket.IO

Authentication:

JWT

bcrypt

Database

Use:

MySQL

Reason:

Simple

Relational

Matches your PRD tables.

OCR

Use:

Tesseract OCR

Face Verification (optional simplified)

Use:

OpenCV
or

face-api.js
```

---
```
4. Pages Your Web App Must Have

Based on your PRD flow.

Public Pages

Landing page

Login

Register

Onboarding Pages

Eligibility questionnaire

Document upload

OCR autofill form

Face verification

User Dashboard

Apply for account

View application status

eKYC update

Account overview

Admin Dashboard

Application review

Risk analysis

Approve / reject

Analytics
```
---
# Other Misc Things we can include 

```
5. Key Features You Must Implement

From your PRD:

✔ Eligibility screening
✔ OCR document parsing
✔ Face verification
✔ Risk scoring
✔ Admin review workflow
✔ Real-time updates
✔ Secure data masking

These are explicitly required in the PRD. 

_(PRD)

6. Documentation You Must Include

Inside /docs:

Problem statement

System architecture

Application flow

Database schema

API endpoints

Security model

✅ Next step I recommend (VERY important before coding):

We should design the Database Schema properly based on the PRD tables.

This will decide:

Users table

Applications table

EKYC table

Audit logs

And it will make your backend 10x easier to implement.

If you want, I can also show you the exact ER diagram your project should have.
```