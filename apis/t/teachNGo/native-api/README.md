# Teach 'n Go: Native API Reference

A consolidated summary of Teach 'n Go's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://intercom.help/teach-n-go/en/collections/3322148-integrations-apis
- **API base URL:** `https://app.teachngo.com`

## Authentication

### API Key

Authenticate Teach 'n Go requests with an API key generated in School Settings > Developers.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://intercom.help/teach-n-go/en/articles/8727904-teach-n-go-api-endpoints)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

The total page count is read from `totalPages`. The current page number is read from `page`.

## Pagination

Use `per_page` in the request body to set the page size (default 20; accepted range 1–200).

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Student Note](actions/add-student-note.md) | `POST /api/v1/note/add` | [docs](https://intercom.help/teach-n-go/en/articles/9123701-add-a-student-note-using-the-api) |
| [Create Prospect](actions/create-prospect.md) | `POST /LeadsApi/add` | [docs](https://intercom.help/teach-n-go/en/articles/5750592-prospect-registration-api) |
| [Create Student](actions/create-student.md) | `POST /api/student` | [docs](https://intercom.help/teach-n-go/en/articles/6807235-new-student-and-class-registration-api) |
| [Enrol Prospect in Lesson](actions/enrol-prospect-in-lesson.md) | `POST /globalApis/enrollProspect` | [docs](https://intercom.help/teach-n-go/en/articles/5750592-prospect-registration-api) |
| [Enroll Student in Class](actions/enroll-student-in-class.md) | `POST /api/enrollclass` | [docs](https://intercom.help/teach-n-go/en/articles/8948828-existing-student-class-enrollment-api) |
| [List Courses](actions/list-courses.md) | `POST /globalApis/course_list` | [docs](https://intercom.help/teach-n-go/en/articles/8727904-teach-n-go-api-endpoints) |
| [List Lessons](actions/list-lessons.md) | `POST /globalApis/lesson_list/:course_id` | [docs](https://intercom.help/teach-n-go/en/articles/8727904-teach-n-go-api-endpoints) |
| [List Payments](actions/list-payments.md) | `POST /api/v1/payments` | [docs](https://intercom.help/teach-n-go/en/articles/8727904-teach-n-go-api-endpoints) |
| [List Prospects](actions/list-prospects.md) | `POST /globalApis/prospect_list` | [docs](https://intercom.help/teach-n-go/en/articles/8727904-teach-n-go-api-endpoints) |
| [List Receipts](actions/list-receipts.md) | `POST /api/v1/receipts` | [docs](https://intercom.help/teach-n-go/en/articles/8727904-teach-n-go-api-endpoints) |
| [List Student Attendance](actions/list-student-attendance.md) | `POST /globalApis/students_attendance` | [docs](https://intercom.help/teach-n-go/en/articles/8727904-teach-n-go-api-endpoints) |
| [List Student Behaviours](actions/list-student-behaviours.md) | `POST /globalApis/student_behaviours` | [docs](https://intercom.help/teach-n-go/en/articles/8727904-teach-n-go-api-endpoints) |
| [List Students](actions/list-students.md) | `POST /globalApis/student_list` | [docs](https://intercom.help/teach-n-go/en/articles/8727904-teach-n-go-api-endpoints) |
