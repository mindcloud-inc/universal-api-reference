# List Project SSH Users with mittwald

Retrieves project SSH users from mittwald API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/:projectId/ssh-users`
- **Base URL:** `https://api.mittwald.de`
- **Official documentation:** [List Project SSH Users](https://api.mittwald.de/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The unique identifier of the project. |
