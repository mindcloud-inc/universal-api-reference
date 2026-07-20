# Add Student to Course with Xperiencify

Creates a student enrollment in an Xperiencify course.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/public/student/create/`
- **Base URL:** `https://api.xperiencify.io`
- **Official documentation:** [Add Student to Course](https://intercom.help/xperiencify/en/articles/9888509-integrating-with-the-api#h_6ebaea9e33)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `student_email` | body | `string` | yes | Email address for the student. |
| `first_name` | body | `string` | yes | Student first name. |
| `last_name` | body | `string` | no | Student last name. |
| `phone` | body | `string` | no | Student phone number. |
| `course_id` | body | `number` | yes | Course to enroll the student in. |
| `password` | body | `string` | no | Optional password for the student. |
