# Get a goal with Asana

Retrieves a goal from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `goals/:goal_gid`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get a goal](https://developers.asana.com/reference/getgoal)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `goal_gid` | path | `string` | yes | Path parameter: goal_gid |
| `opt_fields[]` | query | `array<string>` | no | — |
