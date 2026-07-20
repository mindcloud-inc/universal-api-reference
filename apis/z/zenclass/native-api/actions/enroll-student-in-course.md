# Enroll student in course with Zenclass

Enrolls an existing student in a Zenclass course.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/student/course/enroll`
- **Base URL:** `https://api.zenclass.net`
- **Official documentation:** [Enroll student in course](https://docs.zenclass.ru)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | body | `string` | yes | Zenclass course UUID. |
| `data.send_email` | body | `boolean` | no | Whether Zenclass should email the student. |
| `data.tariff_id` | body | `string` | no | Course tariff UUID. |
| `data.valid_to` | body | `date` | no | Access expiration timestamp. |
| `email` | body | `string` | yes | Student email address. |
