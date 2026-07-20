# Generate Report with Timing

Retrieves a time and app usage report from Timing.

## Endpoint

- **Method:** `GET`
- **Path:** `/report`
- **Base URL:** `https://web.timingapp.com/api/v1`
- **Official documentation:** [Generate Report](https://web.timingapp.com/docs/#reports-GETapi-v1-report)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `start_date_min` | query | `string` | no |
| `start_date_max` | query | `string` | no |
| `projects[]` | query | `array<string>` | no |
