# <img src="https://images.mindcloud.co/apps/icons/zenclass_1776781044624.png" alt="Zenclass logo" width="28" height="28"> Zenclass: Universal API

Manage Zenclass schools, students, enrollments, and access links

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zenclass/latest
- **Category:** Human Resources / Learning (LMS)
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://zenclass.ru
- **Vendor API docs:** https://docs.zenclass.ru

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get school](actions/get-school.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenclass/latest/actions/get-school?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### Auto Login Link

| Action | Method | Description |
| --- | --- | --- |
| [Create auto login link](actions/create-auto-login-link.md) | POST | Creates a one-click login link in Zenclass. |

### Course Access

| Action | Method | Description |
| --- | --- | --- |
| [Change course tariff](actions/change-course-tariff.md) | PUT | Updates a student's course tariff in Zenclass. |
| [Change course validity](actions/change-course-validity.md) | PUT | Updates a student's course access end date in Zenclass. |
| [Confirm course application](actions/confirm-course-application.md) | PUT | Confirms a student's application to a Zenclass course. |
| [Decline course application](actions/decline-course-application.md) | PUT | Declines a student's application to a Zenclass course. |
| [Enroll student in course](actions/enroll-student-in-course.md) | POST | Enrolls an existing student in a Zenclass course. |
| [Expel student from course](actions/expel-student-from-course.md) | PUT | Expels a student from a Zenclass course. |
| [Grant full course access](actions/grant-full-course-access.md) | PUT | Grants a student full access to a Zenclass course. |
| [Reinstate student to course](actions/reinstate-student-to-course.md) | PUT | Reinstates a student in a Zenclass course. |
| [Reset course tariff](actions/reset-course-tariff.md) | PUT | Resets a student's course tariff in Zenclass. |

### School

| Action | Method | Description |
| --- | --- | --- |
| [Get school](actions/get-school.md) | GET | Retrieves your school details from Zenclass. |

### Student

| Action | Method | Description |
| --- | --- | --- |
| [Create student](actions/create-student.md) | POST | Creates a new student profile in Zenclass. |
| [Delete student](actions/delete-student.md) | DELETE | Deletes an existing student profile from Zenclass. |
| [Expel student from school](actions/expel-student-from-school.md) | PUT | Expels a student from your Zenclass school. |
| [Reinstate student to school](actions/reinstate-student-to-school.md) | PUT | Reinstates a student in your Zenclass school. |
| [Update student](actions/update-student.md) | PUT | Updates an existing student profile in Zenclass. |

