# <img src="https://images.mindcloud.co/apps/icons/images-17_1774902617638.jpeg" alt="Classe365 logo" width="28" height="28"> Classe365: Universal API

Classe365 is a school management platform and student information system for managing academics, students, staff, attendance, grading, invoicing, CRM, agents, and tasks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/classe365/latest
- **Actions:** 41
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.classe365.com
- **Vendor API docs:** https://speca.io/classe365/academics

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Academic Sessions](actions/list-academic-sessions.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/classe365/latest/actions/list-academic-sessions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (41)

### Academic Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Academic Item](actions/get-academic-item.md) | GET | Retrieves an academic item from Classe365 by type and ID. |

### Academic Session

| Action | Method | Description |
| --- | --- | --- |
| [List Academic Sessions](actions/list-academic-sessions.md) | GET | Retrieves a list of academic sessions from Classe365. |

### Academic Structure

| Action | Method | Description |
| --- | --- | --- |
| [Get Academic Structure](actions/get-academic-structure.md) | GET | Retrieves the academic structure from Classe365. |

### Account Entry

| Action | Method | Description |
| --- | --- | --- |
| [List Account Entries](actions/list-account-entries.md) | GET | Retrieves a list of account entries from Classe365. |

### Admin

| Action | Method | Description |
| --- | --- | --- |
| [List Admins](actions/list-admins.md) | GET | Retrieves a list of admins from Classe365. |
| [Upsert Admin](actions/upsert-admin.md) | POST | Creates or updates an admin in Classe365. |

### Agent

| Action | Method | Description |
| --- | --- | --- |
| [List Agents](actions/list-agents.md) | GET | Retrieves a list of agents from Classe365. |
| [Upsert Agent](actions/upsert-agent.md) | POST | Creates or updates an agent in Classe365. |

### Assessment

| Action | Method | Description |
| --- | --- | --- |
| [List Assessments](actions/list-assessments.md) | GET | Retrieves a list of assessments from Classe365. |

### Assessment Score

| Action | Method | Description |
| --- | --- | --- |
| [Get Multiple Student Assessment Scores](actions/get-multiple-student-assessment-scores.md) | GET | Retrieves assessment scores for multiple students from Classe365. |
| [Get Student Assessment Scores](actions/get-student-assessment-scores.md) | GET | Retrieves assessment scores for one student from Classe365. |
| [Get Subject Assessment Scores](actions/get-subject-assessment-scores.md) | GET | Retrieves assessment scores for one subject from Classe365. |
| [Upsert Assessment Score](actions/upsert-assessment-score.md) | POST | Creates or updates an assessment score in Classe365. |

### Attendance Record

| Action | Method | Description |
| --- | --- | --- |
| [Get Attendance by Date](actions/get-attendance-by-date.md) | GET | Retrieves attendance data from Classe365 for a specific date. |
| [Get Attendance by Date (Linear View)](actions/get-attendance-by-date-linear-view.md) | GET | Retrieves attendance data in linear view from Classe365. |
| [Get Attendance Data](actions/get-attendance-data.md) | GET | Retrieves attendance data for students from Classe365. |
| [Upsert Attendance](actions/upsert-attendance.md) | POST | Creates or updates attendance in Classe365. |

### Attendance Setting

| Action | Method | Description |
| --- | --- | --- |
| [Get Attendance Settings](actions/get-attendance-settings.md) | GET | Retrieves attendance configuration settings from Classe365. |

### Class

| Action | Method | Description |
| --- | --- | --- |
| [Upsert Class](actions/upsert-class.md) | POST | Creates or updates a class in Classe365. |

### Course Enrollment

| Action | Method | Description |
| --- | --- | --- |
| [Enroll Student in Course](actions/enroll-student-in-course.md) | POST | Enrolls a student in a course in Classe365. |

### Department

| Action | Method | Description |
| --- | --- | --- |
| [Upsert Department](actions/upsert-department.md) | POST | Creates or updates a department in Classe365. |

### Elective Subject Enrollment

| Action | Method | Description |
| --- | --- | --- |
| [Enroll Student in Elective Subject](actions/enroll-student-in-elective-subject.md) | POST | Enrolls a student in an elective subject in Classe365. |

### Fee Invoice

| Action | Method | Description |
| --- | --- | --- |
| [List Fee Invoices](actions/list-fee-invoices.md) | GET | Retrieves a list of fee invoices from Classe365. |

### Fee Record

| Action | Method | Description |
| --- | --- | --- |
| [Get Fee Records](actions/get-fee-records.md) | GET | Retrieves fee, invoice, or payment records from Classe365. |

### Form Submission

| Action | Method | Description |
| --- | --- | --- |
| [Get Form Submission](actions/get-form-submission.md) | GET | Retrieves a form submission from Classe365. |
| [List Submissions](actions/list-submissions.md) | GET | Retrieves a list of submissions from Classe365. |
| [Upsert Form Submission](actions/upsert-form-submission.md) | POST | Creates or updates a form submission in Classe365. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST | Creates a new invoice in Classe365. |

### Ledger Account

| Action | Method | Description |
| --- | --- | --- |
| [List Ledger Accounts](actions/list-ledger-accounts.md) | GET | Retrieves a list of ledger accounts from Classe365. |

### Section

| Action | Method | Description |
| --- | --- | --- |
| [Upsert Section](actions/upsert-section.md) | POST | Creates or updates a section in Classe365. |

### Student

| Action | Method | Description |
| --- | --- | --- |
| [List Students](actions/list-students.md) | GET | Retrieves a list of students from Classe365. |
| [Upsert Student](actions/upsert-student.md) | POST | Creates or updates a student in Classe365. |

### Student Attribute

| Action | Method | Description |
| --- | --- | --- |
| [List Student Attributes](actions/list-student-attributes.md) | GET | Retrieves a list of student attributes from Classe365. |

### Student Count

| Action | Method | Description |
| --- | --- | --- |
| [Get Total Student Count](actions/get-total-student-count.md) | GET | Retrieves the total student count from Classe365. |

### Student Status

| Action | Method | Description |
| --- | --- | --- |
| [Change Student Status](actions/change-student-status.md) | PUT | Updates a student's status in Classe365. |

### Student Subject Status

| Action | Method | Description |
| --- | --- | --- |
| [Update Student Subject Status](actions/update-student-subject-status.md) | PUT | Updates a student's subject status in Classe365. |

### Subject

| Action | Method | Description |
| --- | --- | --- |
| [Upsert Subject](actions/upsert-subject.md) | POST | Creates or updates a subject in Classe365. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Classe365. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves a list of tasks from Classe365. |

### Teacher

| Action | Method | Description |
| --- | --- | --- |
| [List Teachers](actions/list-teachers.md) | GET | Retrieves a list of teachers from Classe365. |
| [Upsert Teacher](actions/upsert-teacher.md) | POST | Creates or updates a teacher in Classe365. |

