# List Available Times with Samedi

Retrieves available appointment times from Samedi.

## Endpoint

- **Method:** `GET`
- **Path:** `/booking/v3/times`
- **Base URL:** `https://patient.samedi.de/api`
- **Official documentation:** [List Available Times](https://api-docs.samedi.de/booking-api/appointment-data/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_category_id` | query | `string` | yes | Appointment category ID to search available times for. |
| `event_type_id` | query | `string` | yes | Appointment type ID to search available times for. |
| `date` | query | `date` | no | Optional date to search available times for. |
| `from` | query | `date` | no | Optional start date for availability range. |
| `to` | query | `date` | no | Optional end date for availability range. |
| `insurance_id` | query | `string` | no | Optional insurance company ID used to filter available times. |
