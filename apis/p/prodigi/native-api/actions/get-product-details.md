# Get Product Details with Prodigi

Retrieves details for a specific Prodigi product SKU.

## Endpoint

- **Method:** `GET`
- **Path:** `/products/[:sku]`
- **Base URL:** `https://api.prodigi.com/v4.0`
- **Official documentation:** [Get Product Details](https://www.prodigi.com/print-api/docs/reference/#get-product-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sku` | path | `string` | yes | Prodigi product SKU to retrieve. |
