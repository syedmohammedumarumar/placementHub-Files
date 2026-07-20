placementhub-frontend/ l

├── public/
│
├── src/
│
│── assets/
│   ├── images/
│   ├── icons/
│   ├── logos/
│   ├── illustrations/
│   ├── animations/
│   └── fonts/
│
├── components/                     # Reusable Components
│
│   ├── Navbar/
│   │     ├── Navbar.jsx
│   │     └── Navbar.css
│   │
│   ├── Sidebar/
│   │     ├── Sidebar.jsx
│   │     └── Sidebar.css
│   │
│   ├── Footer/
│   │     ├── Footer.jsx
│   │     └── Footer.css
│   │
│   ├── Button/
│   │     ├── Button.jsx
│   │     └── Button.css
│   │
│   ├── Input/
│   │     ├── Input.jsx
│   │     └── Input.css
│   │
│   ├── SearchBar/
│   │     ├── SearchBar.jsx
│   │     └── SearchBar.css
│   │
│   ├── Modal/
│   │     ├── Modal.jsx
│   │     └── Modal.css
│   │
│   ├── Loader/
│   │     ├── Loader.jsx
│   │     └── Loader.css
│   │
│   ├── Pagination/
│   │     ├── Pagination.jsx
│   │     └── Pagination.css
│   │
│   ├── Breadcrumb/
│   │     ├── Breadcrumb.jsx
│   │     └── Breadcrumb.css
│   │
│   ├── EmptyState/
│   │     ├── EmptyState.jsx
│   │     └── EmptyState.css
│   │
│   ├── ErrorState/
│   │     ├── ErrorState.jsx
│   │     └── ErrorState.css
│   │
│   ├── ProtectedRoute/
│   │     ├── ProtectedRoute.jsx
│   │     └── ProtectedRoute.css
│   │
│   └── Toast/
│         ├── Toast.jsx
│         └── Toast.css
│
├── layouts/
│
│   ├── MainLayout/
│   │     ├── MainLayout.jsx
│   │     └── MainLayout.css
│   │
│   └── AuthLayout/
│         ├── AuthLayout.jsx
│         └── AuthLayout.css
│
├── modules/
│
│   ├── authentication/
│   │
│   │     ├── pages/
│   │     │
│   │     │── Login/
│   │     │     ├── Login.jsx
│   │     │     └── Login.css
│   │     │
│   │     │── Register/
│   │     │     ├── Register.jsx
│   │     │     └── Register.css
│   │     │
│   │     │── ForgotPassword/
│   │     │     ├── ForgotPassword.jsx
│   │     │     └── ForgotPassword.css
│   │     │
│   │     └── ProfileSetup/
│   │           ├── ProfileSetup.jsx
│   │           └── ProfileSetup.css
│   │
│   ├── dashboard/
│   │
│   │     ├── Dashboard.jsx
│   │     ├── Dashboard.css
│   │     │
│   │     └── components/
│   │
│   │          ├── WelcomeCard/
│   │          ├── ReadinessScore/
│   │          ├── RecentActivity/
│   │          ├── Notifications/
│   │          ├── QuickActions/
│   │          └── ProgressChart/
│   │
│   ├── profile/
│   │
│   │     ├── Profile.jsx
│   │     ├── Profile.css
│   │     │
│   │     └── components/
│   │
│   │          ├── PersonalDetails/
│   │          ├── ResumeUpload/
│   │          ├── Skills/
│   │          ├── GitHub/
│   │          ├── LinkedIn/
│   │          └── Settings/
│   │
│   ├── company/
│   │
│   │     ├── pages/
│   │     │
│   │     │── CompanyList/
│   │     │
│   │     │── CompanyDetails/
│   │     │
│   │     │── Eligibility/
│   │     │
│   │     └── components/
│   │
│   │          ├── CompanyCard/
│   │          ├── CompanySearch/
│   │          ├── CompanyFilter/
│   │          ├── HiringProcess/
│   │          ├── SkillCard/
│   │          ├── PreparationTips/
│   │          └── EligibilityBadge/
│   │
│   ├── roadmap/
│   │
│   │     ├── pages/
│   │     │
│   │     │── BeginnerRoadmap/
│   │     │
│   │     │── CompanyRoadmap/
│   │     │
│   │     │── Resources/
│   │     │
│   │     │── MockTests/
│   │     │
│   │     │── ProgressTracker/
│   │     │
│   │     └── components/
│   │
│   │          ├── RoadmapCard/
│   │          ├── ResourceCard/
│   │          ├── PDFCard/
│   │          ├── VideoCard/
│   │          ├── NotesCard/
│   │          ├── ProgressBar/
│   │          └── TopicCard/
│   │
│   ├── interview/
│   │
│   │     ├── pages/
│   │     │
│   │     │── ExperienceList/
│   │     │
│   │     │── ExperienceDetails/
│   │     │
│   │     └── components/
│   │
│   │          ├── ExperienceCard/
│   │          ├── TechnicalQuestions/
│   │          ├── HRQuestions/
│   │          ├── CodingQuestions/
│   │          ├── StudentTips/
│   │          └── SearchExperience/
│   │
│   ├── calendar/
│   │
│   │     ├── Calendar.jsx
│   │     ├── Calendar.css
│   │     │
│   │     └── components/
│   │
│   │          ├── CalendarView/
│   │          ├── UpcomingCompanies/
│   │          ├── ScheduleCard/
│   │          ├── DeadlineCard/
│   │          ├── InterviewDate/
│   │          └── NotificationCard/
│   │
│   ├── readiness/
│   │
│   │     ├── Readiness.jsx
│   │     ├── Readiness.css
│   │     │
│   │     └── components/
│   │
│   │          ├── ResumeUpload/
│   │          ├── ResumeAnalysis/
│   │          ├── ScoreCard/
│   │          ├── SkillGap/
│   │          ├── Suggestions/
│   │          ├── CompanyScore/
│   │          └── ReportDownload/
│   │
│   └── discussion/
│
│         ├── pages/
│         │
│         │── Discussions/
│         │
│         │── QuestionDetails/
│         │
│         │── MyQuestions/
│         │
│         └── components/
│
│              ├── DiscussionCard/
│              ├── AskQuestion/
│              ├── Answer/
│              ├── Comment/
│              ├── Reply/
│              ├── Upvote/
│              └── SearchDiscussion/
│
├── hooks/
│
│     ├── useAuth.js
│     ├── useCompanies.js
│     ├── useResources.js
│     ├── useProfile.js
│     └── useLocalStorage.js
│
├── context/
│
│     ├── AuthContext.jsx
│     ├── ThemeContext.jsx
│     ├── UserContext.jsx
│     └── NotificationContext.jsx
│
├── services/
│
│     ├── api.js
│     ├── authService.js
│     ├── dashboardService.js
│     ├── companyService.js
│     ├── roadmapService.js
│     ├── interviewService.js
│     ├── calendarService.js
│     ├── readinessService.js
│     ├── discussionService.js
│     └── profileService.js
│
├── routes/
│
│     ├── AppRoutes.jsx
│     ├── PrivateRoutes.jsx
│     └── PublicRoutes.jsx
│
├── styles/
│
│     ├── global.css
│     ├── variables.css
│     ├── typography.css
│     ├── animations.css
│     └── utilities.css
│
├── utils/
│
│     ├── constants.js
│     ├── validators.js
│     ├── helpers.js
│     ├── storage.js
│     ├── dateFormatter.js
│     └── permissions.js
│
├── App.jsx
├── main.jsx
└── vite.config.js
