# Expel student from course with Zenclass

Expels a student from a Zenclass course.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/student/course/expel`
- **Base URL:** `https://api.zenclass.net`
- **Official documentation:** [Expel student from course](https://docs.zenclass.ru)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | body | `string` | yes | Zenclass course UUID. |
| `email` | body | `string` | yes | Student email address. |
