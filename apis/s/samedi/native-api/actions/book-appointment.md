# Book Appointment with Samedi

Books an appointment in Samedi.

## Endpoint

- **Method:** `POST`
- **Path:** `/booking/v3/book`
- **Base URL:** `https://patient.samedi.de/api`
- **Official documentation:** [Book Appointment](https://api-docs.samedi.de/booking-api/appointment-booking/)

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
| `do_notification` | body | `boolean` | no | Legacy consent flag that enables or disables both email and SMS notifications. |
| `allow_email_notifications` | body | `boolean` | no | Consent flag for email notifications. |
| `allow_sms_notifications` | body | `boolean` | no | Consent flag for SMS notifications. |
| `ref` | body | `string` | no | Optional alphanumeric source identifier for the booking. |
