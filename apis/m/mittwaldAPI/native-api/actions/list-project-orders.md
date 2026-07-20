# List Project Orders with mittwald

Retrieves project orders from mittwald API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/:projectId/orders`
- **Base URL:** `https://api.mittwald.de`
- **Official documentation:** [List Project Orders](https://api.mittwald.de/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The unique identifier of the project. |
