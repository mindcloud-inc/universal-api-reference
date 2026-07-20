# List Location Transactions with BoxHero

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/location-txs`
- **Base URL:** `https://rest.boxhero-app.com`
- **Official documentation:** [List Location Transactions](https://rest.boxhero-app.com/docs/api#/transactions/LocationTxsController_getLocationTxs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cursor` | query | `number` | no | Cursor for the next page of transactions |
| `limit` | query | `number` | no | Maximum number of transactions to return |
| `type` | query | `string` | no | Filter transactions by type |
