# Get Order with Booqable

Retrieves an order from Booqable.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders/:id`
- **Base URL:** `https://mindcloud.booqable.com/api/4`
- **Official documentation:** [Get Order](https://developers.booqable.com/#orders-fetch-an-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The UUID of the order to fetch. |
| `fields[orders]` | query | `string` | no | Comma-separated order fields to include instead of the default fields. |
| `include` | query | `string` | no | Comma-separated relationships to sideload. |
