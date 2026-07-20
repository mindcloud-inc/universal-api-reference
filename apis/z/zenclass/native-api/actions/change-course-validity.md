# Change course validity with Zenclass

Updates a student's course access end date in Zenclass.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/student/course/change_validity`
- **Base URL:** `https://api.zenclass.net`
- **Official documentation:** [Change course validity](https://docs.zenclass.ru)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | body | `string` | yes | Zenclass course UUID. |
| `data.valid_to` | body | `date` | yes | Access expiration timestamp. |
| `email` | body | `string` | yes | Student email address. |
