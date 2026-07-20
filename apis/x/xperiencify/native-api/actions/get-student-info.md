# Get Student Info with Xperiencify

Retrieves student details from Xperiencify by email address.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/public/student/info/`
- **Base URL:** `https://api.xperiencify.io`
- **Official documentation:** [Get Student Info](https://intercom.help/xperiencify/en/articles/9888509-integrating-with-the-api#h_acaa21e682)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Student email address. |
| `course_id` | body | `number` | no | Optional course context for course-specific progress data. |
