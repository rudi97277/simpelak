# Project Planning Document

**Project Name:** Simpleak (Simple Act)  
**Date:** April 28, 2025

---

## 1. Project Objectives

- Launch a functional MVP (Minimum Viable Product) of Simpleak for mobile (Android/iOS) and web within 3–4 months.
- Allow users to report issues anonymously or publicly with GPS/manual location.
- Build an administrator panel to manage users, reports, and moderation.
- Implement an AI-based validation system for user reports.
- Provide a point-based system for report quality for each user.

---

## 2. Project Scope

### In-Scope:

- Mobile and Web App Development (React Native).
- Backend Development (Golang).
- Database Management (PostgreSQL + PostGIS for maps).
- Admin Panel Development.
- Integration of Google OAuth.
- Basic AI system for content validation.
- Public Map and List of reports.

### Out-of-Scope (for Phase 1):

- Multi-language support.
- Real-time notifications.
- Direct government integration/response system.

---

## 3. Project Deliverables

| Deliverable              | Description                                               |
| :----------------------- | :-------------------------------------------------------- |
| Mobile App (Android/iOS) | Available via app stores (or direct APK/IPA for testing). |
| Web App                  | Available via secure web URL.                             |
| Backend API              | Secure RESTful APIs serving mobile and web.               |
| Admin Panel              | Web-based dashboard for admin operations.                 |
| Database Schema          | Well-documented schema for reporting and user management. |
| Deployment               | Hosting on production server (Docker or VPS).             |

---

## 4. Project Milestones

| Milestone                           | Estimated Completion | Notes                                                  |
| :---------------------------------- | :------------------- | :----------------------------------------------------- |
| Finalize BRD and Planning           | Week 1               | Done                                                   |
| UI/UX Wireframes Approval           | Week 2               | Basic screens for mobile/web.                          |
| Backend Setup (API + DB)            | Week 2–3             | Setting up Go project, PostgreSQL, and authentication. |
| Frontend MVP (Basic screens)        | Week 4–5             | Login/Register, Submit Report, View Reports.           |
| AI Moderation Integration (Phase 1) | Week 6–7             | Simple ML model for initial checking.                  |
| Admin Panel Development             | Week 6–8             | Admin dashboard (manage users/reports).                |
| QA Testing Phase                    | Week 9               | Internal + external testers.                           |
| Soft Launch (Beta Release)          | Week 10              | Invite-only or region-limited release.                 |
| Public Launch                       | Week 12              | Full deployment to app stores and production server.   |

---

## 5. Project Timeline Overview

Approximate total project duration: **12 weeks** (3 months)

```plaintext
Week 1-2: Planning, Design
Week 3-5: Backend + Basic Frontend
Week 6-8: Advanced Features (AI, Admin Panel)
Week 9: Testing
Week 10: Beta Launch
Week 11-12: Fixes + Public Launch
```

---

## 6. Team Roles and Responsibilities

| Role                                 | Responsibility                                                |
| :----------------------------------- | :------------------------------------------------------------ |
| Project Manager                      | Overall coordination, timeline tracking, risk management.     |
| Frontend Developer                   | Mobile app and web app using React Native.                    |
| Backend Developer                    | API development, database management using Golang/PostgreSQL. |
| UI/UX Designer                       | Wireframes and prototype designs.                             |
| QA Tester                            | Testing features across devices and browsers.                 |
| AI Engineer (optional/part-time)     | Develop lightweight report validation system.                 |
| DevOps Engineer (optional/part-time) | Assist in Docker setup, CI/CD pipelines, and deployments.     |

---

## 7. Risks and Mitigation Plan

| Risk                   | Mitigation                                                      |
| :--------------------- | :-------------------------------------------------------------- |
| Delay in backend setup | Parallel development of UI and backend mock APIs.               |
| AI system complexity   | Start with simple keyword models before upgrading to NLP-based. |
| Unexpected bugs        | Early QA engagement after each sprint.                          |
| Deployment challenges  | Use containerization (Docker) for predictable deployments.      |

---

## 8. Tools and Technologies

| Area                  | Tool/Technology                    |
| :-------------------- | :--------------------------------- |
| Mobile/Web App        | React Native (Expo/Bare Workflow)  |
| Backend               | Golang (Fiber or Gin framework)    |
| Database              | PostgreSQL + PostGIS               |
| Hosting               | VPS / Dockerized Containers        |
| Authentication        | Google OAuth2 + JWT Tokens         |
| Maps                  | Google Maps SDK / OpenStreetMap    |
| AI Moderation (basic) | Tensorflow Lite / simple ML models |
| Version Control       | Git (GitHub or GitLab)             |
| Project Management    | Jira / Trello                      |

---

## 9. Assumptions

- Team members are available as planned.
- MVP scope does not change significantly.
- External APIs (Google OAuth, Maps) remain stable during development.

---

# End of Document
