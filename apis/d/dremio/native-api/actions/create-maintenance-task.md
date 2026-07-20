# Create Maintenance Task with Dremio

Creates a new maintenance task in a Dremio project.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/maintenance/tasks`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Create Maintenance Task](https://docs.dremio.com/dremio-cloud/api/data-maintenance/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_id` | path | `string` | yes |
| `task` | body | `object` | yes |
| `type` | body | `string` | yes |
