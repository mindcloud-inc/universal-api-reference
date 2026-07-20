# Edusign: Native API Reference

A consolidated summary of Edusign's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developers.edusign.com/reference
- **OpenAPI specification:** https://dash.readme.com/api/v1/api-registry/a9lbjcf7cmfmpbz6r
- **API base URL:** `https://ext.edusign.fr`

## Authentication

### API Key

Authenticate requests with a bearer API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.edusign.com/docs/api-reference)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Students Or Professors To Training](actions/add-students-or-professors-to-training.md) | `POST /v1/trainings/resources/:trainingId` | [docs](https://developers.edusign.com/reference) |
| [Archive Professor](actions/archive-professor.md) | `DELETE /v1/professor/:professorId` | [docs](https://developers.edusign.com/reference) |
| [Archive Student](actions/archive-student.md) | `DELETE /v1/student/:studentId` | [docs](https://developers.edusign.com/reference) |
| [Archive Training](actions/archive-training.md) | `DELETE /v1/trainings/:trainingId` | [docs](https://developers.edusign.com/reference) |
| [Create Course](actions/create-course.md) | `POST /v1/course` | [docs](https://developers.edusign.com/reference) |
| [Create Document Using Base64](actions/create-document-using-base64.md) | `POST /v2/documents` | [docs](https://developers.edusign.com/reference) |
| [Create Event](actions/create-event.md) | `POST /v1/events` | [docs](https://developers.edusign.com/reference) |
| [Create Professor](actions/create-professor.md) | `POST /v1/professor` | [docs](https://developers.edusign.com/reference) |
| [Create Student](actions/create-student.md) | `POST /v1/student` | [docs](https://developers.edusign.com/reference) |
| [Create Survey](actions/create-survey.md) | `POST /v1/surveys` | [docs](https://developers.edusign.com/reference) |
| [Create Training](actions/create-training.md) | `POST /v1/trainings/` | [docs](https://developers.edusign.com/reference) |
| [Delete Course](actions/delete-course.md) | `DELETE /v1/course/:id` | [docs](https://developers.edusign.com/reference) |
| [Get Course By ID](actions/get-course-by-id.md) | `GET /v1/course/:id` | [docs](https://developers.edusign.com/reference) |
| [Get Course ID By API ID](actions/get-course-id-by-api-id.md) | `GET /v1/course/get-id/:apiId` | [docs](https://developers.edusign.com/reference) |
| [Get Course PIN](actions/get-course-pin.md) | `GET /v1/course/pin/:courseId` | [docs](https://developers.edusign.com/reference) |
| [Get Course Timestamps](actions/get-course-timestamps.md) | `GET /v1/course/timestamps/:courseId` | [docs](https://developers.edusign.com/reference) |
| [Get Document By ID](actions/get-document-by-id.md) | `GET /v2/documents/:documentId` | [docs](https://developers.edusign.com/reference) |
| [Get Professor By Email](actions/get-professor-by-email.md) | `GET /v1/professor/by-email/:email` | [docs](https://developers.edusign.com/reference) |
| [Get Professor By ID](actions/get-professor-by-id.md) | `GET /v1/professor/:professorId` | [docs](https://developers.edusign.com/reference) |
| [Get Professor ID By API ID](actions/get-professor-id-by-api-id.md) | `GET /v1/professor/get-id/:apiId` | [docs](https://developers.edusign.com/reference) |
| [Get School](actions/get-school.md) | `GET /v1/school` | [docs](https://developers.edusign.com/reference) |
| [Get Student By Email](actions/get-student-by-email.md) | `GET /v1/student/by-email/:email` | [docs](https://developers.edusign.com/reference) |
| [Get Student By ID](actions/get-student-by-id.md) | `GET /v1/student/:studentId` | [docs](https://developers.edusign.com/reference) |
| [Get Student ID By API ID](actions/get-student-id-by-api-id.md) | `GET /v1/student/get-id/:apiId` | [docs](https://developers.edusign.com/reference) |
| [Get Survey By ID](actions/get-survey-by-id.md) | `GET /v1/surveys/:surveyId` | [docs](https://developers.edusign.com/reference) |
| [Get Training](actions/get-training.md) | `GET /v1/trainings/:trainingId` | [docs](https://developers.edusign.com/reference) |
| [List Courses](actions/list-courses.md) | `GET /v1/course` | [docs](https://developers.edusign.com/reference) |
| [List Document Templates](actions/list-document-templates.md) | `GET /v2/documents/templates` | [docs](https://developers.edusign.com/reference) |
| [List Documents](actions/list-documents.md) | `GET /v2/documents` | [docs](https://developers.edusign.com/reference) |
| [List Events](actions/list-events.md) | `GET /v1/events` | [docs](https://developers.edusign.com/reference) |
| [List Professors](actions/list-professors.md) | `GET /v1/professor` | [docs](https://developers.edusign.com/reference) |
| [List Students](actions/list-students.md) | `GET /v1/student` | [docs](https://developers.edusign.com/reference) |
| [List Students by IDs](actions/list-students-by-ids.md) | `POST /v1/student/by-ids` | [docs](https://developers.edusign.com/reference) |
| [List Surveys](actions/list-surveys.md) | `GET /v1/surveys` | [docs](https://developers.edusign.com/reference) |
| [List Trainings](actions/list-trainings.md) | `GET /v1/trainings/` | [docs](https://developers.edusign.com/reference) |
| [Update Course](actions/update-course.md) | `PATCH /v1/course/` | [docs](https://developers.edusign.com/reference) |
| [Update Professor](actions/update-professor.md) | `PATCH /v1/professor/` | [docs](https://developers.edusign.com/reference) |
| [Update School](actions/update-school.md) | `PATCH /v1/school` | [docs](https://developers.edusign.com/reference) |
| [Update Student](actions/update-student.md) | `PATCH /v1/student/` | [docs](https://developers.edusign.com/reference) |
| [Update Training](actions/update-training.md) | `PUT /v1/trainings/:trainingId` | [docs](https://developers.edusign.com/reference) |
