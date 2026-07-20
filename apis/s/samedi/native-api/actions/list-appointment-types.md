# List Appointment Types with Samedi

Retrieves appointment types from Samedi.

## Endpoint

- **Method:** `GET`
- **Path:** `/booking/v3/event_types`
- **Base URL:** `https://patient.samedi.de/api`
- **Official documentation:** [List Appointment Types](https://api-docs.samedi.de/booking-api/appointment-data/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_category_id` | query | `string` | yes | Appointment category ID to list appointment types for. |
| `insurance_id` | query | `string` | no | Optional insurance company ID used to filter appointment types. |
| `born_on` | query | `date` | no | Optional patient birth date in YYYY-MM-DD format. |
