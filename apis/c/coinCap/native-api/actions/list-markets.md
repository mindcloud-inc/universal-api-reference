# List Markets with CoinCap

Retrieves markets from CoinCap.

## Endpoint

- **Method:** `GET`
- **Path:** `/markets`
- **Base URL:** `https://rest.coincap.io/v3`
- **Official documentation:** [List Markets](https://pro.coincap.io/api-docs/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `exchangeId` | query | `string` | no | Filter by exchange id. |
| `baseSymbol` | query | `string` | no | Filter by base asset symbol. |
| `baseId` | query | `string` | no | Filter by base asset id. |
| `quoteSymbol` | query | `string` | no | Filter by quote asset symbol. |
| `quoteId` | query | `string` | no | Filter by quote asset id. |
| `assetSymbol` | query | `string` | no | Filter by asset symbol on either side of the market. |
| `assetId` | query | `string` | no | Filter by asset id on either side of the market. |
