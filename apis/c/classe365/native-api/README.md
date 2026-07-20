# Classe365: Native API Reference

A consolidated summary of Classe365's API configuration and 41 documented operations, with links to official documentation.

- **Official docs:** https://speca.io/classe365/academics
- **API base URL:** `https://{username}.classe365.com`

## Authentication

### Basic Auth

Authenticate with your Classe365 tenant subdomain as the username and your Classe365 API key as the password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **Subdomain:** `subdomain` · required · Your Classe365 tenant subdomain. Example: if your tenant URL is https://evaluate.classe365.com, enter evaluate.

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://docs.classe365.com/en/articles/460939-classe365-api-introduction)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

Responses from this API use JSON.

## Endpoints (41 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Change Student Status](actions/change-student-status.md) | `POST /rest/studentStatusUpdate` | [docs](https://speca.io/classe365/academics#student-status-change) |
| [Create Invoice](actions/create-invoice.md) | `POST /rest/createInvoice` | [docs](https://speca.io/classe365/academics#create-invoice) |
| [Create Task](actions/create-task.md) | `POST /rest/saveTaskData` | [docs](https://speca.io/classe365/academics#add-task-data) |
| [Enroll Student in Course](actions/enroll-student-in-course.md) | `POST /rest/studentCourseEnroll` | [docs](https://speca.io/classe365/academics#student-course-enrollment) |
| [Enroll Student in Elective Subject](actions/enroll-student-in-elective-subject.md) | `POST /rest/electiveSubjectsAllocation` | [docs](https://speca.io/classe365/academics#manage-elective-subject-allocation) |
| [Get Academic Item](actions/get-academic-item.md) | `GET /rest/getAcademicDataForParticular` | [docs](https://speca.io/classe365/academics#get-data-for-a-particular-department-class-section-or-subject) |
| [Get Academic Structure](actions/get-academic-structure.md) | `GET /rest/getAcademicDataForAll` | [docs](https://speca.io/classe365/academics#get-all-academics-data) |
| [Get Attendance by Date](actions/get-attendance-by-date.md) | `GET /rest/allAttendanceByDate` | [docs](https://speca.io/classe365/academics#get-all-attendance-data-for-particular-date) |
| [Get Attendance by Date (Linear View)](actions/get-attendance-by-date-linear-view.md) | `GET /rest/attendanceByDateInLV` | [docs](https://speca.io/classe365/academics#get-attendance-date-for-all-students-and-particular-date-in-linear-view) |
| [Get Attendance Data](actions/get-attendance-data.md) | `GET /rest/attendanceData` | [docs](https://speca.io/classe365/academics#get-attendance-data) |
| [Get Attendance Settings](actions/get-attendance-settings.md) | `GET /rest/attendanceSettings` | [docs](https://speca.io/classe365/academics#get-attendance-settings) |
| [Get Fee Records](actions/get-fee-records.md) | `GET /rest/feesInfo` | [docs](https://speca.io/classe365/academics#get-fees-data-for-all-fess-particular-fees-particular-invoice-and-particular-payment) |
| [Get Form Submission](actions/get-form-submission.md) | `GET /rest/getSubmission` | [docs](https://speca.io/classe365/academics#get-form-submission-details) |
| [Get Multiple Student Assessment Scores](actions/get-multiple-student-assessment-scores.md) | `GET /rest/studentsScore` | [docs](https://speca.io/classe365/academics#get-assessments-score-for-students) |
| [Get Student Assessment Scores](actions/get-student-assessment-scores.md) | `GET /rest/studentScore` | [docs](https://speca.io/classe365/academics#get-assessment-score-for-student) |
| [Get Subject Assessment Scores](actions/get-subject-assessment-scores.md) | `GET /rest/subjectScore` | [docs](https://speca.io/classe365/academics#get-assessments-score-for-subject) |
| [Get Total Student Count](actions/get-total-student-count.md) | `GET /rest/getTotalStudentCount` | [docs](https://speca.io/classe365/academics#get-total-student-count) |
| [List Academic Sessions](actions/list-academic-sessions.md) | `GET /rest/academicSessions` | [docs](https://speca.io/classe365/academics#get-academic-sessions) |
| [List Account Entries](actions/list-account-entries.md) | `GET /rest/accountEntries` | [docs](https://speca.io/classe365/academics#account-entries) |
| [List Admins](actions/list-admins.md) | `GET /rest/adminsData` | [docs](https://speca.io/classe365/academics#get-admin-data) |
| [List Agents](actions/list-agents.md) | `GET /rest/agentsData` | [docs](https://speca.io/classe365/academics#get-agent-data) |
| [List Assessments](actions/list-assessments.md) | `GET /rest/getAssessments` | [docs](https://speca.io/classe365/academics#get-assessments) |
| [List Fee Invoices](actions/list-fee-invoices.md) | `GET /rest/feeInvoicesData` | [docs](https://speca.io/classe365/academics#get-invoice-data) |
| [List Ledger Accounts](actions/list-ledger-accounts.md) | `GET /rest/ledgerAccounts` | [docs](https://speca.io/classe365/academics#ledger-accounts) |
| [List Student Attributes](actions/list-student-attributes.md) | `GET /rest/studentAttributes` | [docs](https://speca.io/classe365/academics#student-attributes) |
| [List Students](actions/list-students.md) | `GET /rest/studentsData` | [docs](https://speca.io/classe365/academics#get-student-data) |
| [List Submissions](actions/list-submissions.md) | `GET /rest/getSubmissionsData` | [docs](https://speca.io/classe365/academics#get-submissions-deta) |
| [List Tasks](actions/list-tasks.md) | `GET /rest/tasksData` | [docs](https://speca.io/classe365/academics#get-tasks-data) |
| [List Teachers](actions/list-teachers.md) | `GET /rest/teachersData` | [docs](https://speca.io/classe365/academics#get-teacher-data) |
| [Update Student Subject Status](actions/update-student-subject-status.md) | `POST /rest/studentSubjectStatusUpdate` | [docs](https://speca.io/classe365/academics#update-student-subject-status) |
| [Upsert Admin](actions/upsert-admin.md) | `POST /rest/admin` | [docs](https://speca.io/classe365/academics#insert-update-admin) |
| [Upsert Agent](actions/upsert-agent.md) | `POST /rest/agent` | [docs](https://speca.io/classe365/academics#add-or-update-agent) |
| [Upsert Assessment Score](actions/upsert-assessment-score.md) | `POST /rest/saveAssessmentScore` | [docs](https://speca.io/classe365/academics#add-update-assessment-score) |
| [Upsert Attendance](actions/upsert-attendance.md) | `POST /rest/manageAttendance` | [docs](https://speca.io/classe365/academics#attendance) |
| [Upsert Class](actions/upsert-class.md) | `POST /rest/academic` | [docs](https://speca.io/classe365/academics#insert-update-class) |
| [Upsert Department](actions/upsert-department.md) | `POST /rest/academic` | [docs](https://speca.io/classe365/academics#insert-department) |
| [Upsert Form Submission](actions/upsert-form-submission.md) | `POST /rest/formSubmit` | [docs](https://speca.io/classe365/academics#add-or-update-form-submission) |
| [Upsert Section](actions/upsert-section.md) | `POST /rest/academic` | [docs](https://speca.io/classe365/academics#insert-update-section) |
| [Upsert Student](actions/upsert-student.md) | `POST /rest/student` | [docs](https://speca.io/classe365/academics#add-update-student) |
| [Upsert Subject](actions/upsert-subject.md) | `POST /rest/academic` | [docs](https://speca.io/classe365/academics#insert-update-subject) |
| [Upsert Teacher](actions/upsert-teacher.md) | `POST /rest/teacher` | [docs](https://speca.io/classe365/academics#insert-update-teacher) |
