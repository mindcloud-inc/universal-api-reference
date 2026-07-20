# Get Transaction History with Enrich.so

Retrieves credit transaction history from Enrich.so.

## Endpoint

- **Method:** `GET`
- **Path:** `/wallets/transactions`
- **Base URL:** `https://dev.enrich.so/api/v3`
- **Official documentation:** [Get Transaction History](https://doc.enrich.so/get-transaction-history-27483208e0.md)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `string` | no | Optional transaction type filter. |
