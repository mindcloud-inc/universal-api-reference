# Get Product Barcode with Hiboutik

Retrieves a product barcode from Hiboutik.

## Endpoint

- **Method:** `GET`
- **Path:** `/products_barcode/:store_id/:product_id/:size_id/`
- **Base URL:** `https://mindcloudhiboutik20260402.hiboutik.com/api`
- **Official documentation:** [Get Product Barcode](https://mindcloudhiboutik20260402.hiboutik.com/docapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | path | `string` | no | The Hiboutik product id. |
| `size_id` | path | `string` | no | The Hiboutik product size id. |
| `store_id` | path | `string` | no | The Hiboutik store id. |
