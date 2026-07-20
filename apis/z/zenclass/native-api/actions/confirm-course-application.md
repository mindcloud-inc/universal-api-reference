# Confirm course application with Zenclass

Confirms a student's application to a Zenclass course.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/student/course/confirm`
- **Base URL:** `https://api.zenclass.net`
- **Official documentation:** [Confirm course application](https://docs.zenclass.ru)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | body | `string` | yes | Zenclass course UUID. |
| `data.send_email` | body | `boolean` | no | Whether Zenclass should email the student. |
| `email` | body | `string` | yes | Student email address. |
