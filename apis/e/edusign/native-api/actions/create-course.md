# Create Course with Edusign

Creates a new course in Edusign.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/course`
- **Base URL:** `https://ext.edusign.fr`
- **Official documentation:** [Create Course](https://developers.edusign.com/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course` | body | `object` | yes | — |
| `course.NAME` | body | `string` | yes | Name of the course |
| `course.DESCRIPTION` | body | `string` | no | Description of the course |
| `course.START` | body | `string` | yes | Start date of the course (ISO 8601 datetime) |
| `course.END` | body | `string` | yes | End date of the course (ISO 8601 datetime) |
| `course.PROFESSOR` | body | `string` | yes | Professor ID |
| `course.PROFESSOR_2` | body | `string` | no | Professor 2 ID |
| `course.PROFESSOR_3` | body | `string` | no | Professor 3 ID |
| `course.CLASSROOM` | body | `string` | no | Classroom |
| `course.SCHOOL_GROUP[]` | body | `array<string>` | no | — |
| `course.MAX_STUDENTS` | body | `number` | no | Maximum number of students |
| `course.ZOOM` | body | `boolean` | no | Zoom course |
| `course.API_ID` | body | `string` | no | API ID |
| `course.SURVEY_ID` | body | `string` | no | Survey Template ID |
| `course.SURVEY_ID_2` | body | `string` | no | Survey Template ID 2. <br/> It's possible to send several surveys to students |
| `course.SURVEY_1_AUTOMATIC_SEND_DATE` | body | `string` | no | Survey 1 automatic send date (ISO 8601 datetime) |
| `course.SURVEY_2_AUTOMATIC_SEND_DATE` | body | `string` | no | Survey 2 automatic send date (ISO 8601 datetime) |
| `course.TEACHER_SURVEY` | body | `string` | no | Teacher survey ID |
| `course.TRAINING_ID` | body | `string` | no | Training ID |
| `course.NEED_STUDENTS_SIGNATURE` | body | `boolean` | yes | Need students signature |
