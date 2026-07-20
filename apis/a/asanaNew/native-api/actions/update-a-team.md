# Update a team with Asana

Updates a team in Asana.

## Endpoint

- **Method:** `PUT`
- **Path:** `teams/:team_gid`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Update a team](https://developers.asana.com/reference/updateteam)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `team_gid` | path | `string` | yes |
| `data` | body | `object` | yes |
