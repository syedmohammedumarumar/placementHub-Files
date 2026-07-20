placementhub-admin/

├── public/
│
├── src/
│
├── assets/
│   ├── images/
│   ├── icons/
│   ├── logos/
│   ├── illustrations/
│   ├── animations/
│   └── fonts/
│
├── components/                    # Global Reusable Components
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
│   ├── Select/
│   │     ├── Select.jsx
│   │     └── Select.css
│   │
│   ├── TextArea/
│   │     ├── TextArea.jsx
│   │     └── TextArea.css
│   │
│   ├── SearchBar/
│   │     ├── SearchBar.jsx
│   │     └── SearchBar.css
│   │
│   ├── Table/
│   │     ├── Table.jsx
│   │     └── Table.css
│   │
│   ├── DataTable/
│   │     ├── DataTable.jsx
│   │     └── DataTable.css
│   │
│   ├── StatusBadge/
│   │     ├── StatusBadge.jsx
│   │     └── StatusBadge.css
│   │
│   ├── StatCard/
│   │     ├── StatCard.jsx
│   │     └── StatCard.css
│   │
│   ├── Modal/
│   │     ├── Modal.jsx
│   │     └── Modal.css
│   │
│   ├── ConfirmDialog/
│   │     ├── ConfirmDialog.jsx
│   │     └── ConfirmDialog.css
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
│   ├── Toast/
│   │     ├── Toast.jsx
│   │     └── Toast.css
│   │
│   └── FileUpload/
│         ├── FileUpload.jsx
│         └── FileUpload.css
│
├── layouts/
│
│   ├── AdminLayout/
│   │     ├── AdminLayout.jsx
│   │     └── AdminLayout.css
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
│   │     │── ForgotPassword/
│   │     │     ├── ForgotPassword.jsx
│   │     │     └── ForgotPassword.css
│   │     │
│   │     └── AdminProfile/
│   │           ├── AdminProfile.jsx
│   │           └── AdminProfile.css
│   │
│   ├── dashboard/
│   │
│   │     ├── Dashboard.jsx
│   │     ├── Dashboard.css
│   │     │
│   │     └── components/
│   │
│   │          ├── OverviewCards/
│   │          ├── StudentStatistics/
│   │          ├── CompanyStatistics/
│   │          ├── PlacementStatistics/
│   │          ├── RecentActivities/
│   │          ├── UpcomingDrives/
│   │          ├── QuickActions/
│   │          └── Charts/
│   │
│   ├── students/
│   │
│   │     ├── pages/
│   │     │
│   │     │── StudentList/
│   │     │
│   │     │── StudentDetails/
│   │     │
│   │     │── AddStudent/
│   │     │
│   │     │── EditStudent/
│   │     │
│   │     └── components/
│   │
│   │          ├── StudentTable/
│   │          ├── StudentCard/
│   │          ├── StudentSearch/
│   │          ├── StudentFilter/
│   │          ├── ResumeViewer/
│   │          ├── SkillsSection/
│   │          ├── SocialLinks/
│   │          └── BulkUpload/
│   │
│   ├── companies/
│   │
│   │     ├── pages/
│   │     │
│   │     │── CompanyList/
│   │     │
│   │     │── CompanyDetails/
│   │     │
│   │     │── AddCompany/
│   │     │
│   │     │── EditCompany/
│   │     │
│   │     └── components/
│   │
│   │          ├── CompanyTable/
│   │          ├── CompanySearch/
│   │          ├── CompanyFilter/
│   │          ├── EligibilitySection/
│   │          ├── HiringProcess/
│   │          ├── RequiredSkills/
│   │          └── PackageDetails/
│   │
│   ├── learning/
│   │
│   │     ├── pages/
│   │     │
│   │     │── Roadmaps/
│   │     │
│   │     │── Resources/
│   │     │
│   │     │── MockTests/
│   │     │
│   │     └── components/
│   │
│   │          ├── RoadmapTable/
│   │          ├── ResourceTable/
│   │          ├── PDFUpload/
│   │          ├── VideoUpload/
│   │          ├── NotesUpload/
│   │          ├── QuestionManager/
│   │          └── CategoryManager/
│   │
│   ├── interview/
│   │
│   │     ├── pages/
│   │     │
│   │     │── ExperienceList/
│   │     │
│   │     │── ExperienceDetails/
│   │     │
│   │     │── AddExperience/
│   │     │
│   │     │── EditExperience/
│   │     │
│   │     └── components/
│   │
│   │          ├── ExperienceTable/
│   │          ├── TechnicalQuestions/
│   │          ├── HRQuestions/
│   │          ├── CodingQuestions/
│   │          ├── StudentTips/
│   │          └── CompanySelector/
│   │
│   ├── calendar/
│   │
│   │     ├── pages/
│   │     │
│   │     │── Calendar/
│   │     │
│   │     │── AddEvent/
│   │     │
│   │     │── EditEvent/
│   │     │
│   │     └── components/
│   │
│   │          ├── CalendarView/
│   │          ├── EventTable/
│   │          ├── DeadlineCard/
│   │          ├── ScheduleCard/
│   │          ├── UpcomingDrives/
│   │          └── EventFilter/
│   │
│   ├── readiness/
│   │
│   │     ├── pages/
│   │     │
│   │     │── ReadinessRules/
│   │     │
│   │     │── Reports/
│   │     │
│   │     └── components/
│   │
│   │          ├── ResumeAnalysis/
│   │          ├── SkillRequirements/
│   │          ├── CompanyRequirements/
│   │          ├── ScoreConfiguration/
│   │          ├── Suggestions/
│   │          └── ReportTable/
│   │
│   ├── discussion/
│   │
│   │     ├── pages/
│   │     │
│   │     │── DiscussionList/
│   │     │
│   │     │── DiscussionDetails/
│   │     │
│   │     └── components/
│   │
│   │          ├── DiscussionTable/
│   │          ├── DiscussionSearch/
│   │          ├── ModerationPanel/
│   │          ├── Answers/
│   │          ├── Comments/
│   │          └── Reports/
│   │
│   ├── reports/
│   │
│   │     ├── pages/
│   │     │
│   │     │── StudentReports/
│   │     │
│   │     │── CompanyReports/
│   │     │
│   │     │── PlacementReports/
│   │     │
│   │     └── components/
│   │
│   │          ├── ReportCards/
│   │          ├── Charts/
│   │          ├── ExportButtons/
│   │          ├── Filters/
│   │          └── Statistics/
│   │
│   └── settings/
│
│         ├── pages/
│         │
│         │── GeneralSettings/
│         │
│         │── RolesPermissions/
│         │
│         │── SystemSettings/
│         │
│         └── components/
│
│              ├── ThemeSettings/
│              ├── RoleTable/
│              ├── PermissionTable/
│              ├── NotificationSettings/
│              └── SecuritySettings/
│
├── hooks/
│
│     ├── useAuth.js
│     ├── useStudents.js
│     ├── useCompanies.js
│     ├── useReports.js
│     ├── useCalendar.js
│     ├── useDiscussion.js
│     ├── useLearning.js
│     └── useLocalStorage.js
│
├── context/
│
│     ├── AuthContext.jsx
│     ├── ThemeContext.jsx
│     ├── AdminContext.jsx
│     ├── NotificationContext.jsx
│     └── PermissionContext.jsx
│
├── services/
│
│     ├── api.js
│     ├── authService.js
│     ├── dashboardService.js
│     ├── studentService.js
│     ├── companyService.js
│     ├── learningService.js
│     ├── interviewService.js
│     ├── calendarService.js
│     ├── readinessService.js
│     ├── discussionService.js
│     ├── reportService.js
│     └── settingsService.js
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
│     ├── permissions.js
│     └── exportUtils.js
│
├── App.jsx
├── main.jsx
└── vite.config.js