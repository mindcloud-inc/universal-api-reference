# List Available Days with Samedi

Retrieves available appointment days from Samedi.

## Endpoint

- **Method:** `GET`
- **Path:** `/booking/v3/dates`
- **Base URL:** `https://patient.samedi.de/api`
- **Official documentation:** [List Available Days](https://api-docs.samedi.de/booking-api/appointment-data/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_category_id` | query | `string` | yes | Appointment category ID to search available days for. |
| `event_type_id` | query | `string` | yes | Appointment type ID to search available days for. |
| `date` | query | `date` | no | Optional date used to return available days for the date's month. |
| `from` | query | `date` | no | Optional start date for availability range. |
| `to` | query | `date` | no | Optional end date for availability range. |
| `insurance_id` | query | `string` | no | Optional insurance company ID used to filter available days. |
| `born_on` | query | `date` | no | Optional patient birth date in YYYY-MM-DD format. |
