# List Transactions with Shippo - Legacy

Retrieves existing shipping labels from Shippo.

## Endpoint

- **Method:** `GET`
- **Path:** `/transactions`
- **Base URL:** `https://api.goshippo.com`
- **Official documentation:** [List Transactions](https://docs.goshippo.com/shippoapi/public-api/transactions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `results` | path | `string` | no | — |
| `rate` | query | `string` | no | — |
| `results` | query | `string` | no | — |
| `apiKey` | path | `string` | no | Override the authentication API key here. |
