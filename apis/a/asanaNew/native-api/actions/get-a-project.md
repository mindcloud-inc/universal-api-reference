# Get a project with Asana

Retrieves a project from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `projects/:project_gid`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get a project](https://developers.asana.com/reference/getproject)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_gid` | path | `string` | yes |
| `opt_pretty` | query | `boolean` | no |
| `opt_fields` | query | `list<string>` | no |
