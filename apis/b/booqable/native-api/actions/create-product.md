# Create Product with Booqable

Creates a new product in Booqable.

## Endpoint

- **Method:** `POST`
- **Path:** `/products`
- **Base URL:** `https://mindcloud.booqable.com/api/4`
- **Official documentation:** [Create Product](https://developers.booqable.com/#products-create-a-product)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | Product payload. Enter the inner JSON:API resource object, for example type plus attributes. |
| `include` | query | `string` | no | Comma-separated relationships to sideload, for example barcode,inventory_levels,photo. |
