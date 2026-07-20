# Get a time period with Asana

Retrieves a time period from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `time_periods/:time_period_gid`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get a time period](https://developers.asana.com/reference/gettimeperiod)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `opt_fields[]` | query | `array<string>` | no | — |
| `time_period_gid` | path | `string` | yes | Path parameter: time_period_gid |
