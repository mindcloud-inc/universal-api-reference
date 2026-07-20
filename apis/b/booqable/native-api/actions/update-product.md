# Update Product with Booqable

Updates an existing product in Booqable.

## Endpoint

- **Method:** `PUT`
- **Path:** `/products/:id`
- **Base URL:** `https://mindcloud.booqable.com/api/4`
- **Official documentation:** [Update Product](https://developers.booqable.com/#products-update-a-product)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Product ID. |
| `data` | body | `object` | yes | Product payload. Enter the inner JSON:API resource object; the path ID must match the product being updated. |
| `include` | query | `string` | no | Comma-separated relationships to sideload, for example barcode,inventory_levels,photo. |
