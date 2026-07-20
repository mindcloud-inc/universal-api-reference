# Get a project status with Asana

Retrieves a project status from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `project_statuses/:project_status_gid`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get a project status](https://developers.asana.com/reference/getprojectstatus)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_status_gid` | path | `string` | yes |
| `opt_pretty` | query | `boolean` | no |
| `opt_fields` | query | `list<string>` | no |
