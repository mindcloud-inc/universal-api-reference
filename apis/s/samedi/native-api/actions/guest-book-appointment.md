# Guest Book Appointment with Samedi

Books an appointment in Samedi for a guest.

## Endpoint

- **Method:** `POST`
- **Path:** `/booking/v3/book`
- **Base URL:** `https://patient.samedi.de/api`
- **Official documentation:** [Guest Book Appointment](https://api-docs.samedi.de/booking-api/appointment-booking/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_category_id` | body | `string` | yes | Appointment category ID for the booking. |
| `event_type_id` | body | `string` | yes | Appointment type ID for the booking. |
| `starts_at` | body | `string` | yes | Selected appointment start timestamp. |
| `attendant[data][first_name]` | body | `string` | no | Patient first name for booking without a samedi patient user. |
| `attendant[data][last_name]` | body | `string` | no | Patient last name for booking without a samedi patient user. |
| `attendant[data][email]` | body | `string` | no | Patient email for booking without a samedi patient user. |
