# Update Basic Student Info with Xperiencify

Updates a student's basic information in Xperiencify.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/public/student/update/`
- **Base URL:** `https://api.xperiencify.io`
- **Official documentation:** [Update Basic Student Info](https://intercom.help/xperiencify/en/articles/9888509-integrating-with-the-api#h_e7f1a14bd1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `student_email` | body | `string` | yes | Email address for the student. |
| `first_name` | body | `string` | no | Updated first name. |
| `last_name` | body | `string` | no | Updated last name. |
| `phone` | body | `string` | no | Updated phone number. |
| `password` | body | `string` | no | Updated password. |
