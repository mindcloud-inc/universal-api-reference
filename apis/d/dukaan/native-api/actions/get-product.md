# Get Product with Dukaan

Retrieves a product from a Dukaan store.

## Endpoint

- **Method:** `GET`
- **Path:** `api/product/seller/:storeUuid/product/:productUuid/v2/`
- **Base URL:** `https://api.mydukaan.io`
- **Official documentation:** [Get Product](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `storeUuid` | path | `string` | yes | Dukaan store UUID from developer settings. |
| `productUuid` | path | `string` | yes | Dukaan product UUID. |
