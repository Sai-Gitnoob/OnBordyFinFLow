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
```
4. Pages on  Web App Must Have: 

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

Apply for an account

View application status

eKYC update

Account overview

Admin Dashboard

Application review

Risk analysis

Approve/reject

Analytics
```
---
# Other Misc Things we can include 

```
5. Key Features

✔ Eligibility screening
✔ OCR document parsing
✔ Face verification
✔ Risk scoring
✔ Admin review workflow
✔ Real-time updates
✔ Secure data masking

These are explicitly required in the PRD. 

_(PRD)

6. Documentation  Must Include

Inside /docs:

Problem statement

System architecture

Application flow

Database schema

API endpoints

Security model
