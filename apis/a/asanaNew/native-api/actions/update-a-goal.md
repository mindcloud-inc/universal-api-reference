# Update a goal with Asana

Updates a goal in Asana.

## Endpoint

- **Method:** `PUT`
- **Path:** `goals/:goal_gid`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Update a goal](https://developers.asana.com/reference/updategoal)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data` | body | `string` | yes |
| `goal_gid` | path | `string` | yes |
| `opt_pretty` | query | `boolean` | no |
| `opt_fields` | query | `list<string>` | no |
