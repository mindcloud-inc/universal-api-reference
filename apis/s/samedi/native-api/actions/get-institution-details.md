# Get Institution Details with Samedi

Retrieves institution details from Samedi.

## Endpoint

- **Method:** `GET`
- **Path:** `/booking/v3/practices/:practiceId`
- **Base URL:** `https://patient.samedi.de/api`
- **Official documentation:** [Get Institution Details](https://api-docs.samedi.de/booking-api/appointment-data/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `practice_id` | path | `string` | yes | Institution/practice ID to retrieve required patient fields for. |
