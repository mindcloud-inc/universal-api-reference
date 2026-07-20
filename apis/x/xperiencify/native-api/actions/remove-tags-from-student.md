# Remove Tags from Student with Xperiencify

Deletes tags from a student in Xperiencify.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/public/student/tag/manager/`
- **Base URL:** `https://api.xperiencify.io`
- **Official documentation:** [Remove Tags from Student](https://intercom.help/xperiencify/en/articles/9888509-integrating-with-the-api#h_4b331bbfab)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `student_email` | body | `string` | yes | Email address for the student. |
| `tagname` | body | `string` | yes | One or more tag names separated by commas. |
