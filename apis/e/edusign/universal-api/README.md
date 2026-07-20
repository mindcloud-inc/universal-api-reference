# <img src="https://images.mindcloud.co/apps/icons/edusign_1775762694309.png" alt="Edusign logo" width="28" height="28"> Edusign: Universal API

Manage attendance, documents, surveys, and training operations

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/edusign/latest
- **Category:** Human Resources / Learning (LMS)
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://edusign.com
- **Vendor API docs:** https://developers.edusign.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get School](actions/get-school.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/edusign/latest/actions/get-school?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Attendance Record

| Action | Method | Description |
| --- | --- | --- |
| [Get Course Timestamps](actions/get-course-timestamps.md) | GET | Retrieves course timestamps from Edusign. |

### Course

| Action | Method | Description |
| --- | --- | --- |
| [Create Course](actions/create-course.md) | POST | Creates a new course in Edusign. |
| [Delete Course](actions/delete-course.md) | DELETE | Deletes an existing course from Edusign. |
| [Get Course By ID](actions/get-course-by-id.md) | GET | Retrieves a course from Edusign by ID. |
| [Get Course ID By API ID](actions/get-course-id-by-api-id.md) | GET | Retrieves a course ID from Edusign by API ID. |
| [Get Course PIN](actions/get-course-pin.md) | GET | Retrieves a course PIN from Edusign. |
| [List Courses](actions/list-courses.md) | GET | Retrieves courses from Edusign. |
| [Update Course](actions/update-course.md) | PUT | Updates an existing course in Edusign. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Create Document Using Base64](actions/create-document-using-base64.md) | POST | Creates a new document in Edusign from Base64. |
| [Get Document By ID](actions/get-document-by-id.md) | GET | Retrieves a document from Edusign by ID. |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents from Edusign. |

### Document Template

| Action | Method | Description |
| --- | --- | --- |
| [List Document Templates](actions/list-document-templates.md) | GET | Retrieves document templates from Edusign. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | POST | Creates a new event in Edusign. |
| [List Events](actions/list-events.md) | GET | Retrieves events from Edusign. |

### Professor

| Action | Method | Description |
| --- | --- | --- |
| [Archive Professor](actions/archive-professor.md) | DELETE | Archives an existing professor in Edusign. |
| [Create Professor](actions/create-professor.md) | POST | Creates a new professor in Edusign. |
| [Get Professor By Email](actions/get-professor-by-email.md) | GET | Finds a professor in Edusign by email address. |
| [Get Professor By ID](actions/get-professor-by-id.md) | GET | Retrieves a professor from Edusign by ID. |
| [Get Professor ID By API ID](actions/get-professor-id-by-api-id.md) | GET | Retrieves a professor ID from Edusign by API ID. |
| [List Professors](actions/list-professors.md) | GET | Retrieves professors from Edusign. |
| [Update Professor](actions/update-professor.md) | PUT | Updates an existing professor in Edusign. |

### School

| Action | Method | Description |
| --- | --- | --- |
| [Get School](actions/get-school.md) | GET | Retrieves your school details from Edusign. |
| [Update School](actions/update-school.md) | PUT | Updates your school details in Edusign. |

### Student

| Action | Method | Description |
| --- | --- | --- |
| [Archive Student](actions/archive-student.md) | DELETE | Archives an existing student in Edusign. |
| [Create Student](actions/create-student.md) | POST | Creates a new student in Edusign. |
| [Get Student By Email](actions/get-student-by-email.md) | GET | Finds a student in Edusign by email address. |
| [Get Student By ID](actions/get-student-by-id.md) | GET | Retrieves a student from Edusign by ID. |
| [Get Student ID By API ID](actions/get-student-id-by-api-id.md) | GET | Retrieves a student ID from Edusign by API ID. |
| [List Students](actions/list-students.md) | GET | Retrieves students from Edusign. |
| [List Students by IDs](actions/list-students-by-ids.md) | GET | Retrieves students from Edusign by ID list. |
| [Update Student](actions/update-student.md) | PUT | Updates an existing student in Edusign. |

### Survey

| Action | Method | Description |
| --- | --- | --- |
| [Create Survey](actions/create-survey.md) | POST | Creates a new survey in Edusign. |
| [Get Survey By ID](actions/get-survey-by-id.md) | GET | Retrieves a survey from Edusign by ID. |
| [List Surveys](actions/list-surveys.md) | GET | Retrieves surveys from Edusign. |

### Training

| Action | Method | Description |
| --- | --- | --- |
| [Add Students Or Professors To Training](actions/add-students-or-professors-to-training.md) | POST | Adds students or professors to a training in Edusign. |
| [Archive Training](actions/archive-training.md) | DELETE | Archives an existing training in Edusign. |
| [Create Training](actions/create-training.md) | POST | Creates a new training in Edusign. |
| [Get Training](actions/get-training.md) | GET | Retrieves a training from Edusign by ID. |
| [List Trainings](actions/list-trainings.md) | GET | Retrieves trainings from Edusign. |
| [Update Training](actions/update-training.md) | PUT | Updates an existing training in Edusign. |

