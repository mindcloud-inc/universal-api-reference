# Get Asset Markets with CoinCap

Retrieves markets for an asset from CoinCap.

## Endpoint

- **Method:** `GET`
- **Path:** `/assets/:slug/markets`
- **Base URL:** `https://rest.coincap.io/v3`
- **Official documentation:** [Get Asset Markets](https://pro.coincap.io/api-docs/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | path | `string` | yes | The asset slug to retrieve markets for. |
