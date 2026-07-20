# List Maintenance Tasks with Dremio

Retrieves maintenance tasks from a Dremio project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/maintenance/tasks`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [List Maintenance Tasks](https://docs.dremio.com/dremio-cloud/api/data-maintenance/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | yes | Common Expression Language (CEL) filter, for example type=="OPTIMIZE"&&level=="TABLE". |
| `project_id` | path | `string` | yes | — |
