# Firewall Log Analysis Platform

A full-stack modular platform for uploading, parsing, and analyzing firewall logs, with role-based access control and anomaly detection.

## Features
- JWT authentication with access/refresh token rotation
- RBAC with granular permission guards and audit logging
- Multi-format firewall log parsing (Cisco ASA, Fortigate, Windows Defender)
- Anomaly detection and statistics dashboard
- PDF/CSV report export
- Angular frontend with reactive state management

## Tech Stack
**Backend:** NestJS, TypeScript, PostgreSQL, JWT, TypeORM  
**Frontend:** Angular, TypeScript, Angular Material

## Setup

### Backend
```bash
cd backend
cp .env.example .env   # Fill in your values
npm install
npm run start:dev
```

### Frontend
```bash
cd frontend
npm install
ng serve --open
```
