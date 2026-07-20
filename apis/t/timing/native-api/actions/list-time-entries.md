# List Time Entries with Timing

Retrieves all time entries from Timing.

## Endpoint

- **Method:** `GET`
- **Path:** `/time-entries`
- **Base URL:** `https://web.timingapp.com/api/v1`
- **Official documentation:** [List Time Entries](https://web.timingapp.com/docs/#time-entries-GETapi-v1-time-entries)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `start_date_min` | query | `string` | no |
| `start_date_max` | query | `string` | no |
| `projects[]` | query | `array<string>` | no |
