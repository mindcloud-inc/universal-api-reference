# List Assets with CoinCap

Retrieves assets from CoinCap.

## Endpoint

- **Method:** `GET`
- **Path:** `/assets`
- **Base URL:** `https://rest.coincap.io/v3`
- **Official documentation:** [List Assets](https://pro.coincap.io/api-docs/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search by asset slug or symbol. |
| `ids` | query | `string` | no | Comma-separated asset IDs to include. |
