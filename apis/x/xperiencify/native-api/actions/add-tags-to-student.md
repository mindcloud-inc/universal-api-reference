# Add Tags to Student with Xperiencify

Updates a student's tags in Xperiencify.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/public/student/tag/manager/`
- **Base URL:** `https://api.xperiencify.io`
- **Official documentation:** [Add Tags to Student](https://intercom.help/xperiencify/en/articles/9888509-integrating-with-the-api#h_287215e459)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `student_email` | body | `string` | yes | Email address for the student. |
| `tagname` | body | `string` | yes | One or more tag names separated by commas. |
