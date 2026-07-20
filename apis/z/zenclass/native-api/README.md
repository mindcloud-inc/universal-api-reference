# Zenclass: Native API Reference

A consolidated summary of Zenclass's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://docs.zenclass.ru
- **OpenAPI specification:** https://docs.zenclass.ru/openapi.json
- **API base URL:** `https://api.zenclass.net`

## Authentication

### API key

Use a Zenclass API token generated in your school settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.zenclass.ru/article/15035)

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Change course tariff](actions/change-course-tariff.md) | `POST /api/v1/student/course/change_tariff` | [docs](https://docs.zenclass.ru) |
| [Change course validity](actions/change-course-validity.md) | `POST /api/v1/student/course/change_validity` | [docs](https://docs.zenclass.ru) |
| [Confirm course application](actions/confirm-course-application.md) | `POST /api/v1/student/course/confirm` | [docs](https://docs.zenclass.ru) |
| [Create auto login link](actions/create-auto-login-link.md) | `POST /api/v1/auto_login_link` | [docs](https://docs.zenclass.ru) |
| [Create student](actions/create-student.md) | `POST /api/v1/student` | [docs](https://docs.zenclass.ru) |
| [Decline course application](actions/decline-course-application.md) | `POST /api/v1/student/course/decline` | [docs](https://docs.zenclass.ru) |
| [Delete student](actions/delete-student.md) | `DELETE /api/v1/student` | [docs](https://docs.zenclass.ru) |
| [Enroll student in course](actions/enroll-student-in-course.md) | `POST /api/v1/student/course/enroll` | [docs](https://docs.zenclass.ru) |
| [Expel student from course](actions/expel-student-from-course.md) | `POST /api/v1/student/course/expel` | [docs](https://docs.zenclass.ru) |
| [Expel student from school](actions/expel-student-from-school.md) | `POST /api/v1/student/expel` | [docs](https://docs.zenclass.ru) |
| [Get school](actions/get-school.md) | `GET /api/v1/school` | [docs](https://docs.zenclass.ru) |
| [Grant full course access](actions/grant-full-course-access.md) | `POST /api/v1/student/course/grant_access` | [docs](https://docs.zenclass.ru) |
| [Reinstate student to course](actions/reinstate-student-to-course.md) | `POST /api/v1/student/course/reinstate` | [docs](https://docs.zenclass.ru) |
| [Reinstate student to school](actions/reinstate-student-to-school.md) | `POST /api/v1/student/reinstate` | [docs](https://docs.zenclass.ru) |
| [Reset course tariff](actions/reset-course-tariff.md) | `POST /api/v1/student/course/reset_tariff` | [docs](https://docs.zenclass.ru) |
| [Update student](actions/update-student.md) | `PUT /api/v1/student` | [docs](https://docs.zenclass.ru) |
