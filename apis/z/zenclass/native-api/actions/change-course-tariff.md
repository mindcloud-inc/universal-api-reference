# Change course tariff with Zenclass

Updates a student's course tariff in Zenclass.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/student/course/change_tariff`
- **Base URL:** `https://api.zenclass.net`
- **Official documentation:** [Change course tariff](https://docs.zenclass.ru)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | body | `string` | yes | Zenclass course UUID. |
| `data.tariff_id` | body | `string` | yes | Course tariff UUID. |
| `email` | body | `string` | yes | Student email address. |
