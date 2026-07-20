# Get Client Activity Stats with Dext

Retrieves client activity statistics from Dext.

## Endpoint

- **Method:** `GET`
- **Path:** `/clients/:client_id/activity-stats`
- **Base URL:** `https://api.precision.dext.com`
- **Official documentation:** [Get Client Activity Stats](https://help.dext.com/en/articles/272702-data-health-insights-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | path | `string` | yes | The Dext client identifier. |
