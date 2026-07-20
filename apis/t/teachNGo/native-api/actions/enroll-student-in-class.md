# Enroll Student in Class with Teach 'n Go

Enrolls a student in a Teach 'n Go class.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/enrollclass`
- **Base URL:** `https://app.teachngo.com`
- **Official documentation:** [Enroll Student in Class](https://intercom.help/teach-n-go/en/articles/8948828-existing-student-class-enrollment-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | body | `string` | yes | The class or course ID to enrol the student into. |
| `student_id` | body | `string` | yes | The existing student ID to enrol. |
| `enrolment_date` | body | `date` | yes | The enrolment date in YYYY-MM-DD format. |
| `unenrolment_date` | body | `date` | no | The optional unenrolment date in YYYY-MM-DD format. |
