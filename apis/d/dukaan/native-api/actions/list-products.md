# List Products with Dukaan

Retrieves products from a Dukaan store.

## Endpoint

- **Method:** `GET`
- **Path:** `api/seller-front/:storeUuid/product-list/`
- **Base URL:** `https://api.mydukaan.io`
- **Official documentation:** [List Products](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `storeUuid` | path | `string` | yes | Dukaan store UUID from the store developer settings. |
