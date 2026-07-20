# List Project Volumes with mittwald

Retrieves project volumes from mittwald API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/:projectId/volumes`
- **Base URL:** `https://api.mittwald.de`
- **Official documentation:** [List Project Volumes](https://api.mittwald.de/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The unique identifier of the project. |
