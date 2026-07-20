# Delete a project status with Asana

Deletes a project status from Asana.

## Endpoint

- **Method:** `DELETE`
- **Path:** `project_statuses/:project_status_gid`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Delete a project status](https://developers.asana.com/reference/deleteprojectstatus)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_status_gid` | path | `string` | yes |
| `opt_pretty` | query | `boolean` | no |
