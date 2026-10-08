# RSTPL HRMS - Enterprise SaaS Platform
**Brand:** RS Technovisions XpertSkillCop  
**Tagline:** Smart HR Solutions for a Smarter Tomorrow  
**Brand Positioning:** Modern | Intelligent | Secure | Scalable | AI-Powered | Employee-Centric

---

## 1. Product Overview
**RSTPL HRMS** is a commercial-grade, multi-tenant enterprise Human Resource Management System (HRMS) and Payroll SaaS platform designed for manufacturing plants, heavy industries, corporate offices, healthcare facilities, and retail enterprises.

The application integrates real-time biometric IoT attendance hardware (eSSL, ZKTeco, Matrix, Suprema), statutory Indian payroll compliance (EPF 12%, ESIC, PT, TDS), Employee Self-Service (ESS), Manager Self-Service (MSS), Applicant Tracking System (ATS), Performance Management (PMS), automated official HR document generators, and Google Gemini AI HR intelligence.

---

## 2. Core Functional Modules

### A. Multi-Tenant Architecture & Master Hierarchy
- **Multi-Tenant Isolation:** Database partition by `org_id` with Supabase Row Level Security (RLS).
- **Organization Setup:** Multi-Company, Multi-Branch, Multi-Unit (Corporate, Assembly Plants, Tooling Units).
- **Organizational Structure:** Multi-Department, Multi-Designation, Job Grades (L1 to L7), Cost Centres.

### B. Employee Master (360° Profile)
- **Personal Information:** Code, Full Name, DOB, Gender, Blood Group, Marital Status, Emergency Contact.
- **Employment Information:** Joining Date, Confirmation, Employment Type (Full-Time, Contract, Probation), Assigned Shift, Reporting Hierarchy.
- **Statutory Compliance:** PAN, Masked Aadhaar, UAN, EPF eligibility, ESIC eligibility, Bank details (Account Number, IFSC).
- **Salary Breakdown:** Annual CTC, Monthly Basic, HRA, Conveyance, Special Allowance, PF, ESIC, Professional Tax, Net Disbursed.

### C. Time & Attendance Engine
- **Attendance Register:** Daily & monthly views, First IN, Last OUT, total working hours, late arrivals, overtime calculation.
- **Shift Master:** General Shift, Morning Shift A, Afternoon Shift B, Night Shift C with configurable grace periods and half-day thresholds.
- **Attendance Finalization:** Strict lock & review workflow with reason-mandated audit logs prior to payroll processing.

### D. Biometric Machine Integration Studio
- **Vendor Support:** Generic multi-vendor adapter layer supporting eSSL, ZKTeco, Matrix, Suprema, Realtime, BioMax.
- **Features:**
  - `Sync Attendance`: Polls IoT machine hardware via TCP/IP sockets or Push API.
  - `Download Attendance`: Exports raw punch logs to CSV.
  - `Upload Attendance`: Batch import with strict validation and error reporting.
  - `Process Attendance`: Runs shift rules engine against raw punches.
  - `Reprocess Attendance`: Recalculates modified shifts and regularizations.
  - `Finalize Attendance`: Certified payroll handover.

### E. Leave & Field Operations
- **Leave Types:** Casual Leave (CL), Sick Leave (SL), Privilege/Earned Leave (EL), Maternity Leave (ML), Compensatory Off (CO).
- **Policy Engine:** Carry-forward caps, encashment flags, sandwich leave rules.
- **On Duty (OD):** Official client visits and fieldwork authorization.
- **Gate Pass:** Security egress slips for official and personal mid-shift departures.

### F. Self-Service Portals
- **Employee ESS:** Mobile/PWA Geo-attendance punch with GPS verification, leave balance ledger, salary slip downloads.
- **Manager MSS:** Team presence overview, shift adherence, approval queue for leaves and ODs.

### G. Modular Indian Payroll Engine
- **Processing Cycle:** Draft → Validate → Calculate → Review → Approve → Lock → Publish Payslips.
- **Statutory Rules:** EPF (12%), ESIC (0.75%), Maharashtra/Gujarat Professional Tax (PT), TDS estimator.
- **Payslips:** Official printable RSTPL letterhead salary slips.

### H. Talent Acquisition & Development
- **Recruitment ATS:** Requisitions, candidate Kanban pipeline (Applied → Screening → Interview → Selected → Offer → Joined).
- **Performance Management (PMS):** KRA/KPI weightage goals, self and managerial ratings.
- **Training Management:** TNA courses, safety certifications (ISO 45001), participant rosters.

### I. Operations & Assets
- **Expense Claims:** Multi-category reimbursement vouchers with receipt verification.
- **HR Letter Generator:** Appointment, Offer, Increment, Relieving, Warning, and Salary certificates.
- **Asset Management:** IT hardware, laptops, and plant terminal serial number tracking.
- **Exit & Separation:** Notice period tracking, multi-department clearances (IT, Admin, Finance, HR), and F&F settlement.

### J. Google Gemini AI HR Assistant
- Natural language queries respecting RBAC context.
- Answers absenteeism metrics, pending leaves, open vacancies, payroll costs, and biometric device status.

---

## 3. Technology Stack
- **Frontend:** Next.js / React 19, TypeScript, Tailwind CSS, Lucide Icons, Motion.
- **Backend / Database:** Supabase PostgreSQL, Row-Level Security (RLS) policies.
- **AI Integration:** Google Gemini (`@google/genai` TypeScript SDK).
- **Biometric Telemetry:** TCP/IP Push Listener protocol, ADMS, and REST Webhook adapters.

---

## 4. Database Setup & Migrations
The database schema and seeds are located in:
- `src/database/schema.sql` (Production DDL with RLS policies, tables, and constraints)
- `src/database/seed.sql` (Comprehensive enterprise seed data for RSTPL Demo Manufacturing Pvt. Ltd.)

To execute in Supabase SQL Editor:
```sql
-- 1. Execute schema.sql to create tables and RLS policies
-- 2. Execute seed.sql to populate demo plants, shifts, employees, and devices
```

---

## 5. Development & Build
```bash
# Install dependencies
npm install

# Run development server
npm run dev

# Compile and verify production build
npm run build
```

---

## 6. Commercial Contact & Licensing
**Product:** RSTPL HRMS  
**Vendor:** RS Technovisions XpertSkillCop  
**Phone:** +91-8076270151  
**Email:** rstechnovisionsinfo@gmail.com  
**Website:** www.rstechnovisions.co.in  
