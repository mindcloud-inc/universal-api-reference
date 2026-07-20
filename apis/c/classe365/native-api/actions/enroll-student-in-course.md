# Enroll Student in Course with Classe365

Enrolls a student in a course in Classe365.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/studentCourseEnroll`
- **Base URL:** `https://{username}.classe365.com`
- **Official documentation:** [Enroll Student in Course](https://speca.io/classe365/academics#student-course-enrollment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `acds_id` | body | `string` | no | Academic session id. |
| `class_id` | body | `string` | no | Class id. |
| `section_id` | body | `string` | no | Section id. |
| `status` | body | `string` | no | Enrollment status code, such as I for In Progress. |
| `student_id` | body | `string` | no | Student id. |
