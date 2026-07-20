# Remove a collaborator from a goal with Asana

Removes a collaborator from a goal in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `goals/:goal_gid/removeFollowers`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Remove a collaborator from a goal](https://developers.asana.com/reference/removefollowers)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data.followers` | body | `list` | yes |
| `goal_gid` | path | `string` | yes |
| `opt_pretty` | query | `boolean` | no |
| `opt_fields` | query | `list<string>` | no |
