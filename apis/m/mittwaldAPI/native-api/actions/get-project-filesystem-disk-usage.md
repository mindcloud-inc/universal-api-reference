# Get Project Filesystem Disk Usage with mittwald

Retrieves project filesystem disk usage from mittwald API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/:projectId/filesystem-disk-usage`
- **Base URL:** `https://api.mittwald.de`
- **Official documentation:** [Get Project Filesystem Disk Usage](https://api.mittwald.de/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The unique identifier of the project. |
