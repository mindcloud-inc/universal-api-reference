# Create a project in a team with Asana

Creates a project in an Asana team.

## Endpoint

- **Method:** `POST`
- **Path:** `teams/:team_gid/projects`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Create a project in a team](https://developers.asana.com/reference/createprojectforteam)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data` | body | `object` | yes |
| `team_gid` | path | `string` | yes |
