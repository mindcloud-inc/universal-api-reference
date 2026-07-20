# Get goals with Asana

Retrieves goals from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `goals`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get goals](https://developers.asana.com/reference/getgoals)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `is_workspace_level` | query | `boolean` | no |
| `portfolio` | query | `string` | no |
| `project` | query | `string` | no |
| `team` | query | `string` | no |
| `time_periods[]` | query | `array` | no |
| `workspace` | query | `string` | no |
