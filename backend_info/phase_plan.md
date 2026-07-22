# 🎓 PlacementHub — Enterprise Campus Placement Management Platform

PlacementHub is a comprehensive, production-grade enterprise platform designed to manage the end-to-end campus placement process. It connects **Students** with **Placement Officers & Admins** through an interactive, data-driven ecosystem.

---

## 🏛 System Architecture Overview

```text
┌──────────────────────────────────────┐       ┌──────────────────────────────────────┐
│  placementhub-frontend (Student Portal)│       │   placementhub-admin (Admin Console) │
│  React 19 + Vite + Vanilla CSS       │       │   React 19 + Vite + Vanilla CSS      │
└──────────────────┬───────────────────┘       └──────────────────┬───────────────────┘
                   │                                              │
                   └──────────────────────┬───────────────────────┘
                                          │  REST APIs / JSON / JWT
                                          ▼
                      ┌───────────────────────────────────────┐
                      │    placementhub-backend               │
                      │    Spring Boot 3.x | Java 21          │
                      │    Spring Security + JWT              │
                      └───────────────────┬───────────────────┘
                                          │  Spring Data JPA / Hibernate
                                          ▼
                      ┌───────────────────────────────────────┐
                      │    MySQL Database                     │
                      │    Relational Schema & Constraints    │
                      └───────────────────────────────────────┘
```

---

## 🛠 Tech Stack

### Frontend Stack (Completed)
- **Framework:** React 19 + Vite
- **Styling:** Vanilla CSS (CSS Variables, Glassmorphism, Responsive Grid/Flex)
- **Icons:** Lucide React
- **Routing:** React Router v7
- **HTTP Client:** Axios

### Backend Stack (Planned)
- **Language:** Java 21 LTS
- **Framework:** Spring Boot 3.4+
- **Security:** Spring Security 6, JWT (JSON Web Token), BCrypt Password Encoder
- **Persistence:** Spring Data JPA, Hibernate ORM
- **Database:** MySQL 8.x
- **Build Tool:** Apache Maven
- **DTO Mapping:** MapStruct / ModelMapper
- **Boilerplate Reduction:** Lombok
- **API Documentation:** Swagger / Springdoc OpenAPI v3
- **Validation:** Jakarta Bean Validation (`@NotNull`, `@Email`, etc.)
- **File Storage:** Cloudinary SDK (for Student Resumes & Avatars)
- **Email Service:** Spring Boot Starter Mail (SMTP / Thymeleaf HTML Templates)
- **Containerization:** Docker & Docker Compose
- **Testing:** JUnit 5, Mockito, Testcontainers

---

## 📁 Spring Boot Backend Folder Structure

```text
placementhub-backend/
├── pom.xml
├── application.yml
├── README.md
├── Dockerfile
└── src/
    ├── main/
    │   ├── java/
    │   │   └── com/
    │   │       └── placementhub/
    │   │           ├── PlacementHubApplication.java
    │   │           │
    │   │           ├── config/
    │   │           │   ├── SecurityConfig.java
    │   │           │   ├── SwaggerConfig.java
    │   │           │   ├── CloudinaryConfig.java
    │   │           │   ├── CorsConfig.java
    │   │           │   └── ApplicationConfig.java
    │   │           │
    │   │           ├── security/
    │   │           │   ├── JwtTokenProvider.java
    │   │           │   ├── JwtAuthenticationFilter.java
    │   │           │   ├── JwtAuthenticationEntryPoint.java
    │   │           │   ├── CustomUserDetailsService.java
    │   │           │   └── UserPrincipal.java
    │   │           │
    │   │           ├── exception/
    │   │           │   ├── GlobalExceptionHandler.java
    │   │           │   ├── ResourceNotFoundException.java
    │   │           │   ├── BadRequestException.java
    │   │           │   ├── UnauthorizedException.java
    │   │           │   └── ErrorResponse.java
    │   │           │
    │   │           ├── payload/
    │   │           │   ├── ApiResponse.java
    │   │           │   └── PagedResponse.java
    │   │           │
    │   │           ├── constants/
    │   │           │   ├── AppConstants.java
    │   │           │   └── SecurityConstants.java
    │   │           │
    │   │           ├── enums/
    │   │           │   ├── RoleName.java
    │   │           │   ├── PlacementStatus.java
    │   │           │   ├── CompanyType.java
    │   │           │   ├── EventType.java
    │   │           │   └── DifficultyLevel.java
    │   │           │
    │   │           ├── utils/
    │   │           │   ├── AppUtils.java
    │   │           │   └── DateUtils.java
    │   │           │
    │   │           ├── storage/
    │   │           │   ├── FileStorageService.java
    │   │           │   └── CloudinaryStorageServiceImpl.java
    │   │           │
    │   │           ├── notification/
    │   │           │   ├── EmailService.java
    │   │           │   └── NotificationService.java
    │   │           │
    │   │           ├── audit/
    │   │           │   ├── BaseEntity.java
    │   │           │   └── AuditAwareImpl.java
    │   │           │
    │   │           └── modules/
    │   │               ├── auth/
    │   │               │   ├── controller/
    │   │               │   │   └── AuthController.java
    │   │               │   ├── service/
    │   │               │   │   ├── AuthService.java
    │   │               │   │   └── AuthServiceImpl.java
    │   │               │   ├── repository/
    │   │               │   │   └── UserRepository.java
    │   │               │   ├── entity/
    │   │               │   │   ├── User.java
    │   │               │   │   ├── Role.java
    │   │               │   │   └── PasswordResetToken.java
    │   │               │   └── dto/
    │   │               │       ├── LoginRequest.java
    │   │               │       ├── RegisterRequest.java
    │   │               │       ├── JwtAuthResponse.java
    │   │               │       ├── ForgotPasswordRequest.java
    │   │               │       └── ResetPasswordRequest.java
    │   │               │
    │   │               ├── student/
    │   │               │   ├── controller/
    │   │               │   │   └── StudentController.java
    │   │               │   ├── service/
    │   │               │   │   ├── StudentService.java
    │   │               │   │   └── StudentServiceImpl.java
    │   │               │   ├── repository/
    │   │               │   │   └── StudentRepository.java
    │   │               │   ├── entity/
    │   │               │   │   └── StudentProfile.java
    │   │               │   ├── dto/
    │   │               │   │   ├── StudentDto.java
    │   │               │   │   ├── StudentUpdateRequest.java
    │   │               │   │   └── StudentFilterRequest.java
    │   │               │   └── mapper/
    │   │               │       └── StudentMapper.java
    │   │               │
    │   │               ├── company/
    │   │               │   ├── controller/
    │   │               │   │   └── CompanyController.java
    │   │               │   ├── service/
    │   │               │   │   ├── CompanyService.java
    │   │               │   │   └── CompanyServiceImpl.java
    │   │               │   ├── repository/
    │   │               │   │   └── CompanyRepository.java
    │   │               │   ├── entity/
    │   │               │   │   ├── Company.java
    │   │               │   │   ├── EligibilityCriteria.java
    │   │               │   │   └── HiringStep.java
    │   │               │   ├── dto/
    │   │               │   │   ├── CompanyDto.java
    │   │               │   │   └── CompanyRequest.java
    │   │               │   └── mapper/
    │   │               │       └── CompanyMapper.java
    │   │               │
    │   │               ├── roadmap/
    │   │               │   ├── controller/
    │   │               │   │   ├── RoadmapController.java
    │   │               │   │   └── MockTestController.java
    │   │               │   ├── service/
    │   │               │   │   ├── RoadmapService.java
    │   │               │   │   └── MockTestService.java
    │   │               │   ├── repository/
    │   │               │   │   ├── RoadmapRepository.java
    │   │               │   │   ├── TopicRepository.java
    │   │               │   │   ├── MockTestRepository.java
    │   │               │   │   └── StudentProgressRepository.java
    │   │               │   ├── entity/
    │   │               │   │   ├── Roadmap.java
    │   │               │   │   ├── Topic.java
    │   │               │   │   ├── MockTest.java
    │   │               │   │   ├── MockQuestion.java
    │   │               │   │   └── StudentProgress.java
    │   │               │   └── dto/
    │   │               │       ├── RoadmapDto.java
    │   │               │       ├── MockTestDto.java
    │   │               │       └── TestSubmitRequest.java
    │   │               │
    │   │               ├── interview/
    │   │               │   ├── controller/
    │   │               │   │   └── InterviewExperienceController.java
    │   │               │   ├── service/
    │   │               │   │   └── InterviewExperienceService.java
    │   │               │   ├── repository/
    │   │               │   │   └── InterviewExperienceRepository.java
    │   │               │   ├── entity/
    │   │               │   │   └── InterviewExperience.java
    │   │               │   └── dto/
    │   │               │       ├── ExperienceDto.java
    │   │               │       └── ExperienceCreateRequest.java
    │   │               │
    │   │               ├── calendar/
    │   │               │   ├── controller/
    │   │               │   │   └── PlacementCalendarController.java
    │   │               │   ├── service/
    │   │               │   │   └── PlacementCalendarService.java
    │   │               │   ├── repository/
    │   │               │   │   └── PlacementEventRepository.java
    │   │               │   ├── entity/
    │   │               │   │   └── PlacementEvent.java
    │   │               │   └── dto/
    │   │               │       └── PlacementEventDto.java
    │   │               │
    │   │               ├── readiness/
    │   │               │   ├── controller/
    │   │               │   │   └── ReadinessController.java
    │   │               │   ├── service/
    │   │               │   │   ├── ReadinessEngineService.java
    │   │               │   │   └── ReadinessRuleService.java
    │   │               │   ├── repository/
    │   │               │   │   ├── ReadinessScoreRepository.java
    │   │               │   │   └── ReadinessRuleRepository.java
    │   │               │   ├── entity/
    │   │               │   │   ├── ReadinessScore.java
    │   │               │   │   └── ReadinessRule.java
    │   │               │   └── dto/
    │   │               │       └── ReadinessReportDto.java
    │   │               │
    │   │               ├── discussion/
    │   │               │   ├── controller/
    │   │               │   │   └── DiscussionController.java
    │   │               │   ├── service/
    │   │               │   │   └── DiscussionService.java
    │   │               │   ├── repository/
    │   │               │   │   ├── DiscussionQuestionRepository.java
    │   │               │   │   ├── DiscussionAnswerRepository.java
    │   │               │   │   └── QuestionUpvoteRepository.java
    │   │               │   ├── entity/
    │   │               │   │   ├── DiscussionQuestion.java
    │   │               │   │   ├── DiscussionAnswer.java
    │   │               │   │   └── QuestionUpvote.java
    │   │               │   └── dto/
    │   │               │       ├── QuestionDto.java
    │   │               │       ├── AnswerDto.java
    │   │               │       └── CreateQuestionRequest.java
    │   │               │
    │   │               ├── dashboard/
    │   │               │   ├── controller/
    │   │               │   │   └── DashboardController.java
    │   │               │   ├── service/
    │   │               │   │   └── DashboardService.java
    │   │               │   └── dto/
    │   │               │       ├── StudentDashboardStatsDto.java
    │   │               │       └── AdminDashboardStatsDto.java
    │   │               │
    │   │               ├── reports/
    │   │               │   ├── controller/
    │   │               │   │   └── ReportsController.java
    │   │               │   ├── service/
    │   │               │   │   └── ReportsService.java
    │   │               │   └── dto/
    │   │               │       ├── DepartmentReportDto.java
    │   │               │       └── CompanyHiringReportDto.java
    │   │               │
    │   │               └── settings/
    │   │                   ├── controller/
    │   │                   │   └── SettingsController.java
    │   │                   ├── service/
    │   │                   │   └── SettingsService.java
    │   │                   ├── repository/
    │   │                   │   └── SystemSettingRepository.java
    │   │                   └── entity/
    │   │                       └── SystemSetting.java
    │   │
    │   └── resources/
    │       ├── application.yml
    │       ├── application-dev.yml
    │       ├── application-prod.yml
    │       └── templates/
    │           ├── welcome-email.html
    │           └── reset-password.html
    │
    └── test/
        └── java/
            └── com/
                └── placementhub/
                    ├── PlacementHubApplicationTests.java
                    ├── auth/
                    │   └── AuthControllerTest.java
                    └── student/
                        └── StudentServiceTest.java
```

---

## 🗺 Spring Boot Backend Phase Roadmap (Phase 1 to Phase 13)

```text
Database First & Infrastructure
               ↓
Authentication & Role-Based Access Control
               ↓
Core Domain Entities & JPA Repositories
               ↓
Feature Modules (Student, Company, LMS, Experiences, Events)
               ↓
Analytics Engine (Readiness AI, Dashboards & Reports)
               ↓
Discussion Forum & Notifications
               ↓
Testing, Dockerization & Production Deployment
```

---

### 🟢 Phase 1 — Backend Foundation & Infrastructure

#### Phase 1A — Project Setup
- Generate Spring Boot 3.4 project with Java 21, Spring Web, Spring Data JPA, Lombok, Validation, MySQL Driver.
- Configure `application.yml` for multi-environment profiles (`dev`, `prod`).
- Set up Maven wrapper, `.gitignore`, and Git repository structure.
- **Deliverable:** Bootstrapped Spring Boot application connecting cleanly to local MySQL server.

#### Phase 1B — Infrastructure Core
- Implement `BaseEntity` with `@CreatedDate`, `@LastModifiedDate`, `@CreatedBy`, `@LastModifiedBy` using Spring Data JPA Auditing.
- Create standardized API Response wrappers (`ApiResponse<T>`, `PagedResponse<T>`).
- Implement `GlobalExceptionHandler` with `@RestControllerAdvice` handling custom exceptions (`ResourceNotFoundException`, `BadRequestException`, `DuplicateResourceException`).
- Define Application Enums (`RoleName`, `PlacementStatus`, `CompanyType`, `EventType`, `DifficultyLevel`).
- **Deliverable:** Rock-solid production foundation with standardized error handling and response structures.

#### Phase 1C — API Documentation & Health Monitoring
- Integrate Springdoc OpenAPI v3 for Swagger UI (`/swagger-ui.html`).
- Configure Spring Boot Actuator for health check endpoints (`/actuator/health`).
- **Deliverable:** Interactive Swagger documentation UI live and accessible.

---

### 🔐 Phase 2 — Authentication & Security (JWT)

#### Phase 2A — User & Role Domain
- Create `User`, `Role`, and `PasswordResetToken` JPA entities with table indexes and foreign keys.
- Pre-seed standard system roles (`ROLE_STUDENT`, `ROLE_ADMIN`, `ROLE_RECRUITER`) via data initialization runners.

#### Phase 2B — Spring Security 6 Config
- Implement `UserPrincipal` implementing `UserDetails`.
- Implement `CustomUserDetailsService` to fetch user credentials by email.
- Configure `SecurityFilterChain` with stateless session policy, CORS configuration, and public/private endpoint matchers.
- Implement BCrypt password encoder bean.

#### Phase 2C — JWT Authentication Engine
- Build `JwtTokenProvider` generating signed JWT tokens with claims (roles, user ID, expiration).
- Implement `JwtAuthenticationFilter` validating Bearer tokens on incoming HTTP requests.
- Implement `JwtAuthenticationEntryPoint` handling unauthorized access errors (401/403).

#### Phase 2D — Auth APIs & Password Recovery
- Implement `/api/auth/register` (Student registration).
- Implement `/api/auth/login` (Returns JWT token, user info, roles).
- Implement `/api/auth/forgot-password` and `/api/auth/reset-password` flow.
- **Deliverable:** Full JWT authentication lifecycle operational and secured.

---

### 👨🎓 Phase 3 — Student Profile Module

#### Phase 3A — Entity & DTO Mapping
- Create `StudentProfile` entity mapped 1-to-1 with `User`.
- Fields: `usn`, `department`, `batch`, `cgpa`, `backlogs`, `phone`, `skills` (ElementCollection/JSON), `placementStatus`, `companyPlaced`, `resumeUrl`, `resumePublicId`.
- Set up MapStruct `StudentMapper` for DTO conversions.

#### Phase 3B — Student CRUD APIs
- `GET /api/students` (Paginated, searchable by name/USN, filterable by Dept/Status/CGPA/Batch).
- `GET /api/students/{id}` and `GET /api/students/me` (Current logged-in student profile).
- `PUT /api/students/{id}` (Update profile details, skills, contact).
- `DELETE /api/students/{id}` (Admin soft-delete).

#### Phase 3C — Resume & Cloud Storage Integration
- Integrate Cloudinary SDK in `CloudinaryStorageServiceImpl`.
- Implement `POST /api/students/resume` (Upload PDF resume, store in cloud, return public URL & ATS metadata).
- **Deliverable:** Complete student management & resume upload pipeline integrated.

---

### 🏢 Phase 4 — Company & Drive Management Module

#### Phase 4A — Company Domain Model
- Create `Company`, `EligibilityCriteria`, and `HiringStep` entities.
- Fields: `name`, `logoUrl`, `role`, `location`, `packageCtc`, `companyType` (`Product`/`Service`), `status` (`Active`/`Upcoming`/`Closed`), `website`, `description`.

#### Phase 4B — Company APIs
- `GET /api/companies` (Search by query, filter by Type, Status, Package range, Branch eligibility).
- `GET /api/companies/{id}` (Full drive details, eligibility criteria, hiring process steps).
- `POST /api/companies` & `PUT /api/companies/{id}` (Admin add/edit placement drive).
- `DELETE /api/companies/{id}` (Admin delete drive).

#### Phase 4C — Drive Application Engine
- Create `StudentApplication` entity tracking student applications to active company drives.
- `POST /api/companies/{id}/apply` (Validate eligibility rules before allowing application).
- **Deliverable:** Company placement drive lifecycle and eligibility verification complete.

---

### 📚 Phase 5 — Learning LMS & Mock Test Module

#### Phase 5A — Learning Resources Domain
- Create `Roadmap`, `Topic`, and `StudentProgress` entities.
- Support video links, PDF guides, curated practice problems, and step-by-step track ordering.

#### Phase 5B — Mock Test Engine
- Create `MockTest`, `MockQuestion`, and `TestAttempt` entities.
- Fields: test duration, passing score, multi-choice options, correct answer key, explanations.

#### Phase 5C — Learning & Assessment APIs
- `GET /api/roadmaps` and `GET /api/roadmaps/{category}` (Fetch learning tracks).
- `POST /api/topics/{id}/complete` (Toggle student completion status).
- `GET /api/mocktests` and `GET /api/mocktests/{id}` (Fetch questions for quiz session).
- `POST /api/mocktests/{id}/submit` (Evaluate answers, calculate score, record attempt history).
- **Deliverable:** Interactive learning roadmaps and self-assessment engine live.

---

### 💬 Phase 6 — Interview Experience Module

#### Phase 6A — Domain Model
- Create `InterviewExperience` entity.
- Fields: `studentName`, `companyName`, `role`, `packageOffered`, `difficulty`, `overallResult` (`Selected`/`Rejected`), `summary`, `roundDetailsJson`.

#### Phase 6B — Experience APIs
- `GET /api/interview-experiences` (Filter by company name, result status, difficulty).
- `GET /api/interview-experiences/{id}` (Detailed interview experience reading).
- `POST /api/interview-experiences` (Student submission for admin approval/publishing).
- **Deliverable:** Shared peer-to-peer interview experiences repository active.

---

### 📅 Phase 7 — Placement Calendar Module

#### Phase 7A — Domain Model
- Create `PlacementEvent` entity.
- Fields: `title`, `eventType` (`Drive`/`Interview`/`Deadline`/`Talk`), `companyName`, `eventDate`, `venue`, `targetBatch`, `targetBranches`, `description`.

#### Phase 7B — Calendar APIs
- `GET /api/calendar/events` (Filter by month/year or date range).
- `GET /api/calendar/upcoming` (Fetch upcoming deadlines for student dashboard).
- `POST /api/calendar/events` & `DELETE /api/calendar/events/{id}` (Admin event management).
- **Deliverable:** Campus-wide placement event scheduler operational.

---

### 📈 Phase 8 — Placement Readiness AI Module

#### Phase 8A — Readiness Calculation Engine
- Create `ReadinessScore` and `ReadinessRule` entities.
- Algorithm weighs:
  - CGPA Score (25%)
  - Coding / Problem Solving Progress (25%)
  - System Design & Mock Test Scores (25%)
  - Resume ATS Compatibility Score (25%)

#### Phase 8B — Readiness APIs & Rule Config
- `GET /api/readiness/my-score` (Calculates & returns student readiness radar, percentile rank, and company-wise match %).
- `GET /api/readiness/rules` & `PUT /api/readiness/rules` (Admin configures readiness criteria weightages).
- **Deliverable:** Automated placement readiness calculation engine integrated.

---

### 💬 Phase 9 — Community Discussion Forum Module

#### Phase 9A — Discussion Domain Model
- Create `DiscussionQuestion`, `DiscussionAnswer`, and `QuestionUpvote` entities.

#### Phase 9B — Discussion APIs
- `GET /api/discussions` (Paginated, filtered by Category tag, search term, or user questions).
- `GET /api/discussions/{id}` (Question with answers & nested comments).
- `POST /api/discussions` (Ask new question).
- `POST /api/discussions/{id}/answers` (Post answer).
- `POST /api/discussions/{id}/upvote` (Toggle upvote on question or answer).
- **Deliverable:** Collaborative Q&A forum fully functional.

---

### 📊 Phase 10 — Dashboards & Analytics Reports

#### Phase 10A — Dashboard Overview APIs
- `GET /api/dashboard/student` (Student summary metrics: readiness score, applied drives, upcoming events, recent activities).
- `GET /api/dashboard/admin` (Admin KPI summary: total students, placed count, overall placement %, active drives, top recruiters).

#### Phase 10B — Placement Reports & Export APIs
- `GET /api/reports/department` (Department-wise placement statistics breakdown).
- `GET /api/reports/company-hiring` (Company-wise hiring counts & average packages).
- `GET /api/reports/export/csv` (Stream CSV file generation for offline analysis).
- **Deliverable:** Comprehensive visual dashboards and report exporter live.

---

### 📧 Phase 11 — Notifications & Email Service

#### Phase 11A — Mail Sender Engine
- Configure Spring Boot Mail with HTML Thymeleaf templates.
- Automated emails for: Account Welcome, Password Reset Link, Drive Application Confirmation.

#### Phase 11B — In-App Notifications
- Create `Notification` entity for in-app alert badges (Unread count, marked read, drive updates).
- **Deliverable:** Multi-channel notification engine active.

---

### ⚙️ Phase 12 — Production Quality, Auditing & Testing

#### Phase 12A — Performance Optimization
- Implement JPA Specifications for dynamic search/filtering.
- Add pagination (`Pageable`, `Sort`) across all list endpoints.
- Configure query indexing on MySQL columns (`usn`, `email`, `company_name`, `status`).

#### Phase 12B — Testing & Verification
- Unit testing services with JUnit 5 & Mockito.
- Integration testing API controllers using `@SpringBootTest` and `MockMvc`.
- **Deliverable:** Production-tested codebase with high code coverage.

---

### 🐳 Phase 13 — Containerization & Production Deployment

#### Phase 13A — Docker Packaging
- Create optimized multi-stage `Dockerfile` with Java 21 Alpine image.
- Create `docker-compose.yml` linking Spring Boot backend, MySQL container, and persistent volumes.

#### Phase 13B — Deployment Setup
- Deploy backend to Cloud Provider (Railway / Render / AWS EC2).
- Configure environment variables for DB credentials, JWT secret keys, and Cloudinary keys.
- **Deliverable:** Live production REST APIs connected to frontend apps!

---

## 🏆 Complete Project Status & Roadmap Summary

```text
PlacementHub

Phase 1  ➔ Student Frontend      [DONE ✅]
Phase 2  ➔ Admin Frontend        [DONE ✅]
Phase 3  ➔ Spring Boot Backend   [IN PROGRESS 🚀]
Phase 4  ➔ MySQL Database Setup  [PLANNED]
Phase 5  ➔ REST API Integration  [PLANNED]
Phase 6  ➔ Docker & Deployment   [PLANNED]
```
