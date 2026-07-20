# Get Product with Booqable

Retrieves a product from Booqable.

## Endpoint

- **Method:** `GET`
- **Path:** `/products/:id`
- **Base URL:** `https://mindcloud.booqable.com/api/4`
- **Official documentation:** [Get Product](https://developers.booqable.com/#products-fetch-a-product)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Product ID. |
| `include` | query | `string` | no | Comma-separated relationships to sideload, for example barcode,inventory_levels,photo. |
