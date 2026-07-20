# Get Maintenance Task with Dremio

Retrieves a maintenance task from a Dremio project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/maintenance/tasks/:taskId`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Get Maintenance Task](https://docs.dremio.com/dremio-cloud/api/data-maintenance/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_id` | path | `string` | yes |
| `taskId` | path | `string` | yes |
