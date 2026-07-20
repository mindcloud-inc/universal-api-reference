# List Ledgers with e-Boekhouden.nl

Retrieves ledgers from e-Boekhouden.nl.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/ledger`
- **Base URL:** `https://api.e-boekhouden.nl`
- **API:** rest
- **Official documentation:** [List Ledgers](https://api.e-boekhouden.nl/swagger/index.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | The number of items to retrieve. |
| `offset` | query | `number` | no | The number of items to skip. |
| `code` | query | `string` | no | The code of the ledger. Maximum length: 10. |
| `category` | query | `string` | no | The category of the ledger. Maximum length: 10. |
