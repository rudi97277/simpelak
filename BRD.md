# Business Requirements Document (BRD)

**Project Name:** Simpleak (Simple Act)  
**Date:** April 28, 2025

---

## 1. Executive Summary

Simpleak is a community-driven reporting application that enables citizens to easily report public problems such as infrastructure damage, crimes, or public events. Reports can be created via GPS location or manually selected locations, and are shared anonymously on a public platform to drive awareness and faster government response.

The app encourages honest reporting through a points system and uses AI to automatically check reports' validity. It provides both a mobile app and web app experience using React Native, supported by a backend API developed in Go, with PostgreSQL as the database.

---

## 2. Business Objectives

- Facilitate **easy, fast, and anonymous** citizen reporting.
- Improve **government and community response** to public issues.
- Increase **citizen engagement** in public safety and infrastructure monitoring.
- Provide **visibility** of public problems via **maps and lists**.
- Implement **gamification** through a **points system** to encourage valid reporting.

---

## 3. Scope of Work

### In Scope

- User registration (Email and Google OAuth).
- Anonymous or public identity control on reports.
- Report submission with GPS or manual location.
- Voting system to prioritize important reports.
- Report display in both **list** and **map** views.
- AI moderation of new user reports.
- Points system management.
- Administrator dashboard with different permission levels.

### Out of Scope (for Phase 1)

- Direct government communication integration.
- Push notifications.
- Multi-language support.

---

## 4. Key Features & Requirements

| Feature                      | Description                                                                                                                                               |
| :--------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **User Registration/Login**  | Users can register using email/password or Google login.                                                                                                  |
| **Identity Privacy Control** | Users choose whether their identity is visible or anonymous per report.                                                                                   |
| **Report Submission**        | Users submit reports with title, description, category, photo (optional), and location (GPS/manual).                                                      |
| **Voting**                   | Users can vote on reports to increase priority. One vote per report per user.                                                                             |
| **Points System**            | Users start with 0 points. Valid reports increase points. After 70 points, reports are auto-approved with random checks. False reports reset points to 0. |
| **Report Moderation**        | AI checks for fake/spam reports for low-point users. Admins oversee flagged reports.                                                                      |
| **Administrator Management** | Admins can create new admins with full or partial privileges (RBAC).                                                                                      |
| **Report List and Map View** | Reports are shown publicly without revealing identities unless chosen.                                                                                    |
| **Role System**              | General User, Administrator (with sub-roles).                                                                                                             |
| **Mobile + Web Access**      | Accessible via Android/iOS apps and Web app.                                                                                                              |

---

## 5. User Roles

| Role                               | Permissions                                                              |
| :--------------------------------- | :----------------------------------------------------------------------- |
| **General User**                   | Register/login, submit reports, vote on reports, view reports.           |
| **Administrator (Full Access)**    | Manage users, manage reports, create other admins, assign privileges.    |
| **Administrator (Limited Access)** | Access depends on privileges given (e.g., only manage reports or users). |

---

## 6. Technical Requirements

- **Frontend:** React Native (Expo/Bare workflow for Mobile + Web support).
- **Backend:** Golang (Framework: Fiber or Gin).
- **Database:** PostgreSQL with PostGIS (for geolocation data).
- **Hosting:** Cloud VPS or containerized deployment (Docker).
- **Authentication:** OAuth2 (Google), Email/Password (with secure hashing).
- **APIs:** RESTful APIs secured via JWT.

---

## 7. Non-Functional Requirements

- **Performance:** Map and List should load nearby reports within 2 seconds.
- **Security:** End-to-end encryption, secure authentication, OAuth compliance.
- **Scalability:** Able to handle growth from 1,000 to 100,000 users with horizontal scaling.
- **Reliability:** 99.5% uptime SLA target.
- **Privacy:** User identity stays confidential unless user chooses otherwise.

---

## 8. Assumptions

- Users will have GPS-enabled devices.
- Initial launch will target one region/city before expansion.
- Admin team will manually validate edge cases in reports.

---

## 9. Risks and Mitigation

| Risk                         | Mitigation Strategy                                               |
| :--------------------------- | :---------------------------------------------------------------- |
| Fake reports flooding system | AI moderation + Points system + Random manual review.             |
| User privacy breaches        | Strict identity encryption and frontend/backend privacy controls. |
| Low adoption                 | Promote via local government/community partnerships.              |

---

## 10. Dependencies

- Google Cloud for OAuth integration.
- Hosting provider for backend and database.
- Mapping service (Google Maps, Mapbox, or OpenStreetMap).

---

# Appendix

- [A] Draft Wireframe sketches
- [B] API Endpoints Table (to be built later)
- [C] DB ERD Diagram (to be built next)

---
