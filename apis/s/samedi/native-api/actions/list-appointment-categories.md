# List Appointment Categories with Samedi

Retrieves appointment categories from Samedi.

## Endpoint

- **Method:** `GET`
- **Path:** `/booking/v3/event_categories`
- **Base URL:** `https://patient.samedi.de/api`
- **Official documentation:** [List Appointment Categories](https://api-docs.samedi.de/booking-api/appointment-data/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `practice_id` | query | `string` | yes | Institution/practice ID to list appointment categories for. |
| `insurance_id` | query | `string` | no | Optional insurance company ID used to filter appointment categories. |
| `born_on` | query | `date` | no | Optional patient birth date in YYYY-MM-DD format. |
