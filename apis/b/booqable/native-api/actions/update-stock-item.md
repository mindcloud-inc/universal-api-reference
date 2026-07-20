# Update Stock Item with Booqable

Updates an existing stock item in Booqable.

## Endpoint

- **Method:** `PUT`
- **Path:** `/stock_items/:id`
- **Base URL:** `https://mindcloud.booqable.com/api/4`
- **Official documentation:** [Update Stock Item](https://developers.booqable.com/#stock-items-update-a-stock_item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Stock item ID. |
| `data` | body | `object` | yes | Stock item payload. Enter the inner JSON:API resource object; the path ID must match the stock item being updated. |
| `include` | query | `string` | no | Comma-separated relationships to sideload, for example barcode,location,properties. |
