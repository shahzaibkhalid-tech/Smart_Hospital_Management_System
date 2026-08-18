# Smart Hospital Management System (SHMS)

A robust, scalable backend solution for managing hospital operations, patient records, and administrative tasks.

## Tech Stack

- **Framework**: NestJS (Node.js)
- **Language**: TypeScript
- **Database**: PostgreSQL (with Prisma ORM)
- **Documentation**: Swagger UI

## Core Features (Planned)

1. **User Authentication & Authorization**
   - Role-Based Access Control (RBAC)
   - Roles: Admin, Doctor, Patient, Staff
2. **Patient Management**
   - Electronic Health Records (EHR)
   - Patient Registration & Profiles
3. **Appointment Scheduling**
   - Real-time availability for doctors
   - Online booking & rescheduling
4. **Billing & Invoicing**
   - Automated billing generation
   - Integration with payment gateways
5. **Pharmacy & Inventory**
   - Prescription management
   - Medical supply tracking
6. **Reporting & Analytics**
   - Hospital performance metrics
   - Patient flow analysis

## Getting Started

1. Install dependencies: `npm install`
2. Set up environment variables: `cp .env.example .env`
3. Run database migrations: `npx prisma migrate dev`
4. Start the application: `npm run start:dev`
