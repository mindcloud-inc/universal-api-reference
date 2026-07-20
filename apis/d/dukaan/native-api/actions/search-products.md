# Search Products with Dukaan

Finds products in Dukaan by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `api/seller-front/:storeUuid/product-list/`
- **Base URL:** `https://api.mydukaan.io`
- **Official documentation:** [Search Products](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `storeUuid` | path | `string` | yes | Dukaan store UUID from developer settings. |
| `search` | query | `string` | yes | Product search text. |
