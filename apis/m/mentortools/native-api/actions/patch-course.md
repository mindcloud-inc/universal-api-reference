# Patch Course with Mentortools

Updates part of an existing course in Mentortools.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/courses/v1/:course_id`
- **Base URL:** `https://app.mentortools.com/public_api`
- **Official documentation:** [Patch Course](https://app.mentortools.com/public_api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | path | `number` | yes | The course ID. |
| `title` | body | `string` | no | Title of the course, if not provided, it will not be updated. |
