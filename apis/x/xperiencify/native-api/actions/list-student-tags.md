# List Student Tags with Xperiencify

Retrieves tags for a student in Xperiencify.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/public/student/tag/list/`
- **Base URL:** `https://api.xperiencify.io`
- **Official documentation:** [List Student Tags](https://intercom.help/xperiencify/en/articles/9888509-integrating-with-the-api#h_ed3982e551)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `student_email` | query | `string` | yes | Email address for the student. |
