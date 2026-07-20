# Get a team's project templates with Asana

Retrieves a team's project templates from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `teams/:team_gid/project_templates`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get a team's project templates](https://developers.asana.com/reference/getprojecttemplatesforteam)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `limit` | query | `number` | no |
| `offset` | query | `string` | no |
| `team_gid` | path | `string` | yes |
