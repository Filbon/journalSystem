# Medical Journal System (Microservices Architecture)

## Overview
This project is a **microservices-based medical journal system** designed to manage patient records, observations, and communications between medical staff and patients. The system was initially built as a monolithic application and later refactored into multiple services for better scalability and maintainability.

### Tech Stack
- **Backend Services**: Spring Boot, Quarkus Reactive, Node.js
- **Frontend**: React.js
- **Database**: PostgreSQL/MySQL
- **Authentication**: Keycloak
- **Message Queue**: Apache Kafka (for advanced event-driven architecture)
- **Containerization & Orchestration**: Docker, Kubernetes

---

## Microservices Overview
| **Service Name**                  | **Technology**        | **Description** |
|----------------------------------|---------------------|-----------------|
| **ImageProcessing_JournalSys**   | Node.js            | Handles image storage, retrieval, and annotation. |
| **frontend_journalSys**          | React.js           | User interface for patients, doctors, and staff. |
| **searchService_JournalSys**     | Quarkus Reactive   | Enables reactive database searches for patients, conditions, and encounters. |
| **userRoleService_JournalSys**   | Spring Boot        | Manages user roles, patient data, conditions, and encounters. |
| **messageService_JournalSys**    | Spring Boot        | Handles messaging between patients, doctors, and staff. |
| **userService_JournalSys**       | Spring Boot        | Manages user registration, authentication, and account-related operations. |

---

## Features
- **User Authentication & Role-Based Access Control (RBAC)**
- **Medical Record Management** (Patients, Observations, Conditions, Encounters)
- **Messaging System** (Patients ↔ Doctors/Staff)
- **Image Storage & Annotation** (Medical Images)
- **Advanced Search Functionality** (By Name, Condition, Practitioner)
- **CI/CD Pipeline** (Automated Testing & Deployment via GitHub Actions)
- **API Security** (JWT Authentication via Keycloak)

---

### Deployment & CI/CD
This project uses GitHub Actions for CI/CD. When changes are merged into the main branch, the following steps are triggered:

- **Run Unit Tests (JUnit/Postman tests)**
- **Build Docker Images**
- **Deploy Services to Kubernetes**

## Security

- **Authentication: Keycloak for OAuth2 & JWT-based API authentication.**
- **API Security: Spring Security for access control.**
- **Database Security: Role-based access to patient data.**
