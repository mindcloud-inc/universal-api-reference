# Get time periods with Asana

Retrieves time periods from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `time_periods`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get time periods](https://developers.asana.com/reference/gettimeperiods)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `end_on` | query | `date` | no |
| `start_on` | query | `date` | no |
| `workspace` | query | `string` | yes |
