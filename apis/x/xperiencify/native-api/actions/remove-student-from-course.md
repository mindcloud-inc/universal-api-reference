# Remove Student From Course with Xperiencify

Deletes a student's enrollment from an Xperiencify course.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/public/student/course/remove/`
- **Base URL:** `https://api.xperiencify.io`
- **Official documentation:** [Remove Student From Course](https://intercom.help/xperiencify/en/articles/9888509-integrating-with-the-api#h_f8ef3e3a68)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `student_email` | body | `string` | yes | Email address for the student. |
| `course_id` | body | `number` | yes | Course to remove the student from. |
