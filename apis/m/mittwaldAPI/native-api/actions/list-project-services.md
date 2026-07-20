# List Project Services with mittwald

Retrieves project services from mittwald API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/:projectId/services`
- **Base URL:** `https://api.mittwald.de`
- **Official documentation:** [List Project Services](https://api.mittwald.de/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The unique identifier of the project. |
