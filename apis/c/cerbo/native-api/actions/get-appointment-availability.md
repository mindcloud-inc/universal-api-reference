# Get Appointment Availability with Cerbo

Retrieves appointment availability from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/appointments/availability`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Get Appointment Availability](https://docs.cer.bo/#tag/Appointment-Availability/operation/getAppointmentAvailability)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `string` | yes | Starting date of the date range. The start date should be formatted as `YYYY-MM-DD`. |
| `end_date` | query | `string` | yes | Ending date of the date range. The end date should be formatted as `YYYY-MM-DD`. The end date cannot be more than 90 days from the start date. |
| `provider_ids[]` | query | `array<number>` | no | Provider identifiers. If specified, results will be for only those providers. |
| `appointment_type_ids[]` | query | `array<number>` | no | Appointment type identifiers. If specified, results will be for only those appointment types. |
