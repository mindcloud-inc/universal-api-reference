# Get Appointments Report with Zenoti

Returns a simpler result than List Appointments

## Endpoint

- **Method:** `POST`
- **Path:** `reports/appointments/flat_file`
- **Base URL:** `https://api.zenoti.com/v1/`
- **Official documentation:** [Get Appointments Report](none)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appointment_sources[].source` | body | `list` | no | — |
| `appointmentStatuses[].appointmentStatus` | body | `list` | no | — |
| `centerIds[].center` | body | `list` | no | — |
| `date_type` | body | `list` | no | — |
| `center_ids[]` | body | `array` | no | — |
| `date` | body | `date` | no | Use this when getting results for a single date |
| `start_date` | body | `date` | no | — |
| `end_date` | body | `date` | no | — |
| `appointment_statuses[]` | body | `array` | no | — |
| `appointment_sources[]` | body | `array` | no | — |
