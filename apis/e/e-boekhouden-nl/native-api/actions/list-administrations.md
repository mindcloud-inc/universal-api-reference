# List Administrations with e-Boekhouden.nl

Retrieves administrations from e-Boekhouden.nl.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/administration`
- **Base URL:** `https://api.e-boekhouden.nl`
- **API:** rest
- **Official documentation:** [List Administrations](https://api.e-boekhouden.nl/swagger/index.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | The number of items to retrieve. |
| `offset` | query | `number` | no | The number of items to skip. |
