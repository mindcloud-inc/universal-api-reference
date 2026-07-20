# Create Order with Booqable

Creates a new order in Booqable.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders`
- **Base URL:** `https://mindcloud.booqable.com/api/4`
- **Official documentation:** [Create Order](https://developers.booqable.com/#orders-create-an-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | JSON:API order payload with the nested `data` object expected by Booqable. Include `type: orders` and any `attributes` or `relationships` you want to create. |
| `fields[orders]` | query | `string` | no | Comma-separated order fields to include instead of the default fields. |
| `include` | query | `string` | no | Comma-separated relationships to sideload. |
