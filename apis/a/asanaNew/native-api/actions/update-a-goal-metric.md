# Update a goal metric with Asana

Updates a goal metric in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `goals/:goal_gid/setMetricCurrentValue`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Update a goal metric](https://developers.asana.com/reference/updategoalmetric)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `goal_gid` | path | `string` | yes | Path parameter: goal_gid |
| `opt_fields[]` | query | `array<string>` | no | — |
| `data` | body | `object` | yes | — |
