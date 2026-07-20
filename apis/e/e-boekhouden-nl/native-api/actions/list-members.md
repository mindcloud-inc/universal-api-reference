# List Members with e-Boekhouden.nl

Retrieves members from e-Boekhouden.nl for clubs or associations.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/member`
- **Base URL:** `https://api.e-boekhouden.nl`
- **API:** rest
- **Official documentation:** [List Members](https://api.e-boekhouden.nl/swagger/index.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | The number of items to retrieve. |
| `offset` | query | `number` | no | The number of items to skip. |
| `memberNumber` | query | `string` | no | The number of the member. |
| `name` | query | `string` | no | Only retrieves members with this name. |
| `email` | query | `string` | no | Only retrieves members with this e-mailadress. |
| `city` | query | `string` | no | Only retrieves members from this city. |
