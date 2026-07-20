# Reset course tariff with Zenclass

Resets a student's course tariff in Zenclass.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/student/course/reset_tariff`
- **Base URL:** `https://api.zenclass.net`
- **Official documentation:** [Reset course tariff](https://docs.zenclass.ru)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | body | `string` | yes | Zenclass course UUID. |
| `email` | body | `string` | yes | Student email address. |
