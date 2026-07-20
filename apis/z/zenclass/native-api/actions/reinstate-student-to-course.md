# Reinstate student to course with Zenclass

Reinstates a student in a Zenclass course.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/student/course/reinstate`
- **Base URL:** `https://api.zenclass.net`
- **Official documentation:** [Reinstate student to course](https://docs.zenclass.ru)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | body | `string` | yes | Zenclass course UUID. |
| `email` | body | `string` | yes | Student email address. |
