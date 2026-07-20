# List Lessons with Teach 'n Go

Retrieves lessons from a Teach 'n Go course.

## Endpoint

- **Method:** `POST`
- **Path:** `/globalApis/lesson_list/:course_id`
- **Base URL:** `https://app.teachngo.com`
- **Official documentation:** [List Lessons](https://intercom.help/teach-n-go/en/articles/8727904-teach-n-go-api-endpoints)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | path | `string` | yes | The Teach 'n Go course ID to load lessons for. |
