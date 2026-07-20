# List Catalog with Dremio

Retrieves catalog entries from a Dremio project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/catalog`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [List Catalog](https://docs.dremio.com/dremio-cloud/api/catalog/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The Dremio project UUID. |
