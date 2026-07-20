# List Account Activity with Perfit

## Endpoint

- **Method:** `GET`
- **Path:** `/:account/activity`
- **Base URL:** `https://api.myperfit.com/v2`
- **Official documentation:** [List Account Activity](https://developers.myperfit.com/monitoreo/listado-de-actividad)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account` | path | `string` | yes | Perfit account name. |
| `q` | query | `string` | no | Email address to filter activity. |
| `view` | query | `string` | no | Response format. |
| `filters.track_type` | query | `string` | no | Filter by event type. |
| `filters.timestamp.gtrel` | query | `string` | no | Relative start time like now-1h. |
| `filters.timestamp.gt` | query | `date` | no | Absolute start time in ISO-8601 format. |
