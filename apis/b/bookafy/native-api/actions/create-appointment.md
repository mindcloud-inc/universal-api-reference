# Create Appointment with Bookafy

Creates an appointment in Bookafy.

## Endpoint

- **Method:** `POST`
- **Path:** `/appointments`
- **Base URL:** `https://app.bookafy.com/api/v2`
- **Official documentation:** [Create Appointment](https://app.bookafy.com/api-docs/v3/appointments_part1.yaml)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appointment[appointment_date]` | body | `string` | no | Appointment date in YYYY-MM-DD format. |
| `appointment[appointment_end_time]` | body | `string` | no | Appointment end time in Bookafy's displayed time format, for example 11:45 AM. |
| `appointment[appointment_start_time]` | body | `string` | no | Appointment start time in Bookafy's displayed time format, for example 11:30 AM. |
| `appointment[category_id]` | body | `string` | no | Bookafy category ID for the appointment. |
| `appointment[description]` | body | `string` | no | Appointment description value sent to Bookafy. |
| `appointment[duration]` | body | `string` | no | Appointment duration in minutes. |
| `appointment[service_id]` | body | `string` | no | Bookafy service ID for the appointment. |
| `appointment[time_zone]` | body | `string` | no | Bookafy time zone label, for example Central Time (US & Canada). |
| `appointment[title]` | body | `string` | no | Appointment title/notes value sent to Bookafy. |
| `appointment[user_id]` | body | `string` | no | Bookafy staff user ID that owns the appointment. |
| `customer[email]` | body | `string` | no | Customer email address for the appointment. |
| `customer[name]` | body | `string` | no | Customer full name for the appointment. |
| `customer[phone]` | body | `string` | no | Customer phone number for the appointment. |
