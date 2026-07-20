# List Appointments with Bookafy

Retrieves appointments from Bookafy by date range.

## Endpoint

- **Method:** `GET`
- **Path:** `/appointments`
- **Base URL:** `https://app.bookafy.com/api/v2`
- **Official documentation:** [List Appointments](https://app.bookafy.com/api-docs/v3/appointments_part1.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Staff email address to scope the appointment list. |
