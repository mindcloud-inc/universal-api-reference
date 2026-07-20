# Update Maintenance Task with Dremio

Updates an existing maintenance task in a Dremio project.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:project_id/maintenance/tasks/:taskId`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Update Maintenance Task](https://docs.dremio.com/dremio-cloud/api/data-maintenance/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_id` | path | `string` | yes |
| `task` | body | `object` | yes |
| `taskId` | path | `string` | yes |
