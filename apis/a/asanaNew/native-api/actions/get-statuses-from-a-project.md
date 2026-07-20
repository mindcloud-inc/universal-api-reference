# Get statuses from a project with Asana

Retrieves project statuses from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `projects/:project_gid/project_statuses`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get statuses from a project](https://developers.asana.com/reference/getprojectstatusesforproject)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `limit` | query | `number` | no |
| `offset` | query | `string` | no |
| `opt_fields[]` | query | `array` | no |
| `opt_pretty` | query | `boolean` | no |
| `project_gid` | path | `string` | yes |
