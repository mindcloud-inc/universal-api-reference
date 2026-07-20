# Delete Maintenance Task with Dremio

Deletes an existing maintenance task from a Dremio project.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:project_id/maintenance/tasks/:taskId`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Delete Maintenance Task](https://docs.dremio.com/dremio-cloud/api/data-maintenance/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_id` | path | `string` | yes |
| `taskId` | path | `string` | yes |
