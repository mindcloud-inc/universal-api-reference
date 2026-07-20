# List Project Delivery Boxes with mittwald

Retrieves project delivery boxes from mittwald API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/:projectId/delivery-boxes`
- **Base URL:** `https://api.mittwald.de`
- **Official documentation:** [List Project Delivery Boxes](https://api.mittwald.de/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The unique identifier of the project. |
