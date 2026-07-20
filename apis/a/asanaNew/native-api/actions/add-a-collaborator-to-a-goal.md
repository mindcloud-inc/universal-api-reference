# Add a collaborator to a goal with Asana

Adds a collaborator to a goal in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `goals/:goal_gid/addFollowers`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Add a collaborator to a goal](https://developers.asana.com/reference/addfollowers)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data.followers` | body | `list` | yes |
| `goal_gid` | path | `string` | yes |
