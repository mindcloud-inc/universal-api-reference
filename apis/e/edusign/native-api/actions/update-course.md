# Update Course with Edusign

Updates an existing course in Edusign.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/course/`
- **Base URL:** `https://ext.edusign.fr`
- **Official documentation:** [Update Course](https://developers.edusign.com/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course` | body | `object` | yes | — |
| `course.ID` | body | `string` | yes | ID of the course |
| `course.NAME` | body | `string` | no | Name of the course |
| `course.DESCRIPTION` | body | `string` | no | Description of the course |
| `course.START` | body | `string` | no | Start date of the course (ISO 8601 datetime) |
| `course.END` | body | `string` | no | End date of the course (ISO 8601 datetime) |
| `course.PROFESSOR` | body | `string` | no | Professor ID at least one professor is required |
| `course.PROFESSOR_2` | body | `string` | no | Professor 2 ID |
| `course.PROFESSOR_3` | body | `string` | no | Professor 3 ID |
| `course.CLASSROOM` | body | `string` | no | Classroom |
| `course.SCHOOL_GROUP[]` | body | `array<string>` | no | — |
| `course.SURVEY_ID` | body | `string` | no | Survey Template ID |
| `course.SURVEY_ID_2` | body | `string` | no | Survey Template ID 2. <br/> It's possible to send several surveys to students |
| `course.TEACHER_SURVEY` | body | `string` | no | — |
| `course.SURVEY_1_AUTOMATIC_SEND_DATE` | body | `string` | no | Survey 1 automatic send date (ISO 8601 datetime) |
| `course.SURVEY_2_AUTOMATIC_SEND_DATE` | body | `string` | no | Survey 2 automatic send date (ISO 8601 datetime) |
| `course.TEACHER_SURVEY_AUTOMATIC_SEND_DATE` | body | `string` | no | — |
| `course.ZOOM` | body | `boolean` | no | Zoom course |
| `course.API_ID` | body | `string` | no | API ID |
| `course.NEED_STUDENTS_SIGNATURE` | body | `boolean` | yes | Need students signature |
| `course.TRAINING_ID` | body | `string` | no | Training ID. Warning: if a course is already linked to a training and this field is set to null/empty, the course will be unlinked from that training |
| `editSurveys` | body | `boolean` | yes | Boolean query param (true/false), If true and a SURVEY_ID is provided, the survey will be erased and a new will be created. |
