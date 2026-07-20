# Create a goal metric with Asana

Creates a goal metric in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `goals/:goal_gid/setMetric`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Create a goal metric](https://developers.asana.com/reference/creategoalmetric)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data` | body | `string` | yes |
| `goal_gid` | path | `string` | yes |
