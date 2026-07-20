# List Products with e-Boekhouden.nl

Retrieves products from e-Boekhouden.nl.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/product`
- **Base URL:** `https://api.e-boekhouden.nl`
- **API:** rest
- **Official documentation:** [List Products](https://api.e-boekhouden.nl/swagger/index.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | The number of items to retrieve. |
| `offset` | query | `number` | no | The number of items to skip. |
| `code` | query | `string` | no | The code of the product. |
| `groupCode` | query | `string` | no | The product group code. |
