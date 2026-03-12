# System Data Flow (Visual Tagged Architecture)

This section visualizes how data moves through the **OnBordyFinFlow system** using simple operation tags.

Tags used in the system:

INPUT
STORE
FETCH
AUTHENTICATE
VERIFY
CALCULATE
UPDATE

---

# 1. User Registration Flow

INPUT
Email
Phone Number
Username
Password

↓

PROCESS
Hash Password

↓

STORE → Users Table

↓

User Account Created

---

# 2. User Login Flow

INPUT
Email / Phone Number / Username
Password

↓

FETCH → Users Table

↓

AUTHENTICATE → Compare Password Hash

↓

GENERATE SESSION TOKEN

↓

Login Success

---

# 3. Eligibility Screening Flow

INPUT
Age
Income
Employment Status
Residency

↓

CALCULATE → Eligibility Rules

↓

STORE → Eligibility Status

↓

Result

Eligible
Conditionally Eligible
Not Eligible

---

# 4. Document Upload Flow

INPUT
Aadhaar / PAN / Passport

↓

STORE → Documents Table

↓

Document Stored Securely

---

# 5. OCR Extraction Flow

FETCH → Document Image

↓

OCR_PARSE

↓

Extracted Fields

Name
DOB
Address
ID Number

↓

STORE → Structured Data

↓

Auto-Fill Application Form

---

# 6. Face Verification Flow

INPUT → Selfie Image

↓

FETCH → Aadhaar Image

↓

FACE_MATCH

↓

VERIFY → Match Score

↓

UPDATE → Verification Status

---

# 7. Account Application Flow

INPUT → Selected Service

Savings
Current
Salary
FD

↓

STORE → Applications Table

↓

Application Status → Pending Review

---

# 8. Risk Scoring Flow

FETCH
Application Data
Face Match Score
OCR Data

↓

CALCULATE → Risk Score

↓

STORE → Risk Analysis

↓

Risk Category

Low
Medium
High

---

# 9. Admin Review Flow

FETCH → Pending Applications

↓

Admin Decision

APPROVE
REJECT
MANUAL VERIFY

↓

UPDATE → Application Status

---

# 10. Account Activation Flow

After Approval

↓

GENERATE → Account Number

↓

MASK → Sensitive Fields

↓

UPDATE → Activation Status

↓

Account Activated

---

# 11. Audit Logging Flow

Admin Action Performed

↓

STORE → Audit Logs

↓

System Audit Trail Created

---

# Complete End-to-End Data Flow

User Registration
INPUT → STORE

Login
INPUT → FETCH → AUTHENTICATE

Eligibility Screening
INPUT → CALCULATE → STORE

Document Upload
INPUT → STORE

OCR Extraction
FETCH → PARSE → STORE

Face Verification
INPUT → FETCH → VERIFY

Risk Scoring
FETCH → CALCULATE → STORE

Admin Review
FETCH → UPDATE

Account Activation
UPDATE → STORE

Audit Logging
STORE

---

# Tag Summary

INPUT → User provides data
STORE → Save data in database
FETCH → Retrieve data from database
AUTHENTICATE → Verify login credentials
VERIFY → Validate identity or face match
CALCULATE → Compute eligibility or risk score
UPDATE → Modify existing records
