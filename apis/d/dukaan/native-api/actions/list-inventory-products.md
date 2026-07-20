# List Inventory Products with Dukaan

Retrieves inventory products from Dukaan.

## Endpoint

- **Method:** `GET`
- **Path:** `api/product/seller/:storeUuid/product/v2/`
- **Base URL:** `https://api.mydukaan.io`
- **Official documentation:** [List Inventory Products](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `storeUuid` | path | `string` | yes | Dukaan store UUID from developer settings. |
