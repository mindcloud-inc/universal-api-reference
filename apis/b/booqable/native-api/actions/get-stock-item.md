# Get Stock Item with Booqable

Retrieves a stock item from Booqable.

## Endpoint

- **Method:** `GET`
- **Path:** `/stock_items/:id`
- **Base URL:** `https://mindcloud.booqable.com/api/4`
- **Official documentation:** [Get Stock Item](https://developers.booqable.com/#stock-items-fetch-a-stock_item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Stock item ID. |
| `include` | query | `string` | no | Comma-separated relationships to sideload, for example barcode,location,properties. |
