# Get Project Self Membership with mittwald

Retrieves your project membership from mittwald API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/:projectId/memberships/self`
- **Base URL:** `https://api.mittwald.de`
- **Official documentation:** [Get Project Self Membership](https://api.mittwald.de/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The unique identifier of the project. |
