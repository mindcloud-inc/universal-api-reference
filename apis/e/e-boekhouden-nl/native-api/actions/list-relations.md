# List Relations with e-Boekhouden.nl

Retrieves relations from e-Boekhouden.nl.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/relation`
- **Base URL:** `https://api.e-boekhouden.nl`
- **API:** rest
- **Official documentation:** [List Relations](https://api.e-boekhouden.nl/swagger/index.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | The number of items to retrieve. |
| `offset` | query | `number` | no | The number of items to skip. |
| `code` | query | `string` | no | The code of the relation. |
| `type` | query | `string` | no | Business (`B`) or Private (`P`). |
| `email` | query | `string` | no | Only retrieves relations with this e-mailadress. |
| `name` | query | `string` | no | Only retrieves relations with this (company) name. |
| `contact` | query | `string` | no | Only retrieves relations with this contact information. |
| `city` | query | `string` | no | Only retrieves relations from this primary city. |
