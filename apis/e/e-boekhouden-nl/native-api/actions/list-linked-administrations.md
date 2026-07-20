# List Linked Administrations with e-Boekhouden.nl

Retrieves linked administrations from e-Boekhouden.nl.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/administration/linked`
- **Base URL:** `https://api.e-boekhouden.nl`
- **API:** rest
- **Official documentation:** [List Linked Administrations](https://api.e-boekhouden.nl/swagger/index.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | The number of items to retrieve. |
| `offset` | query | `number` | no | The number of items to skip. |
