# Get parent goals from a goal with Asana

Retrieves parent goals for a goal from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `goals/:goal_gid/parentGoals`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get parent goals from a goal](https://developers.asana.com/reference/getparentgoalsforgoal)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `goal_gid` | path | `string` | yes |
| `opt_pretty` | query | `boolean` | no |
| `opt_fields` | query | `list<string>` | no |
