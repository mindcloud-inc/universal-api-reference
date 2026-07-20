# <img src="https://images.mindcloud.co/apps/icons/id-vqzy-b042-logos_1774039988735.jpeg" alt="Teach 'n Go logo" width="28" height="28"> Teach 'n Go: Universal API

Manage students, classes, attendance, payments, and prospects

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/teachNGo/latest
- **Category:** Human Resources / Learning (LMS)
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.teachngo.com
- **Vendor API docs:** https://intercom.help/teach-n-go/en/collections/3322148-integrations-apis

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Students](actions/list-students.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teachNGo/latest/actions/list-students?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [List Student Behaviours](actions/list-student-behaviours.md) | GET | Retrieves student behaviour records from Teach 'n Go. |

### Appointments

| Action | Method | Description |
| --- | --- | --- |
| [List Lessons](actions/list-lessons.md) | GET | Retrieves lessons from a Teach 'n Go course. |

### Attendance Records

| Action | Method | Description |
| --- | --- | --- |
| [List Student Attendance](actions/list-student-attendance.md) | GET | Retrieves student attendance records from Teach 'n Go. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Student](actions/create-student.md) | POST | Creates a new student in Teach 'n Go. |
| [List Students](actions/list-students.md) | GET | Retrieves students from Teach 'n Go. |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [List Receipts](actions/list-receipts.md) | GET | Retrieves receipts from Teach 'n Go. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [List Courses](actions/list-courses.md) | GET | Retrieves courses from Teach 'n Go. |

### Leads

| Action | Method | Description |
| --- | --- | --- |
| [Create Prospect](actions/create-prospect.md) | POST | Creates a new prospect in Teach 'n Go. |
| [List Prospects](actions/list-prospects.md) | GET | Retrieves prospects from Teach 'n Go. |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Add Student Note](actions/add-student-note.md) | POST | Creates a student note in Teach 'n Go. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Enrol Prospect in Lesson](actions/enrol-prospect-in-lesson.md) | POST | Enrols a prospect in a Teach 'n Go lesson. |
| [Enroll Student in Class](actions/enroll-student-in-class.md) | POST | Enrolls a student in a Teach 'n Go class. |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [List Payments](actions/list-payments.md) | GET | Retrieves payments from Teach 'n Go. |

