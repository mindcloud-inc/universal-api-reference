# List Cost Centers with e-Boekhouden.nl

Retrieves cost centers from e-Boekhouden.nl.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/costcenter`
- **Base URL:** `https://api.e-boekhouden.nl`
- **API:** rest
- **Official documentation:** [List Cost Centers](https://api.e-boekhouden.nl/swagger/index.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | The number of items to retrieve. |
| `offset` | query | `number` | no | The number of items to skip. |
| `parentId` | query | `string` | no | The parent ID of the cost center. |
| `description` | query | `string` | no | The description of the cost center. |
