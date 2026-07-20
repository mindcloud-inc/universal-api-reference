# Update Student Subject Status with Classe365

Updates a student's subject status in Classe365.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/studentSubjectStatusUpdate`
- **Base URL:** `https://{username}.classe365.com`
- **Official documentation:** [Update Student Subject Status](https://speca.io/classe365/academics#update-student-subject-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `acds_id` | body | `string` | no | Academic session id. |
| `class_id` | body | `string` | no | Class id. |
| `section_id` | body | `string` | no | Section id. |
| `status` | body | `string` | no | Enrollment status code. |
| `student_id` | body | `string` | no | Student id. |
| `subject_id` | body | `string` | no | Subject id. |
