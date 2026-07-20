# List Variants with Negative Stock with Katana

Lists variants with negative stock in Katana.

## Endpoint

- **Method:** `GET`
- **Path:** `/negative_stock`
- **Base URL:** `https://api.katanamrp.com/v1`
- **Official documentation:** [List Variants with Negative Stock](https://developer.katanamrp.com/reference/getallnegativestock)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location_id` | query | `number` | no | Filters negative stock by a valid location id |
| `variant_id` | query | `number` | no | Filters negative stock by a valid variant id |
| `latest_negative_stock_date_max` | query | `string` | no | Filters negative stock by a latest negative stock date max |
| `latest_negative_stock_date_min` | query | `string` | no | Filters negative stock by a latest negative stock date min |
| `name` | query | `string` | no | Filters negative stock by a name |
| `sku` | query | `string` | no | Filters negative stock by a sku |
| `category` | query | `string` | no | Filters negative stock by a category |
