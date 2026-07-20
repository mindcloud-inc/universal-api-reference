# Grant full course access with Zenclass

Grants a student full access to a Zenclass course.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/student/course/grant_access`
- **Base URL:** `https://api.zenclass.net`
- **Official documentation:** [Grant full course access](https://docs.zenclass.ru)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | body | `string` | yes | Zenclass course UUID. |
| `data.tariff_id` | body | `string` | no | Course tariff UUID. |
| `data.valid_to` | body | `date` | no | Access expiration timestamp. |
| `email` | body | `string` | yes | Student email address. |
