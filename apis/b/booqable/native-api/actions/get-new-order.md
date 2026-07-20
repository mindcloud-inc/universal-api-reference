# Get New Order with Booqable

Retrieves an existing or new order for the current employee in Booqable.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders/new`
- **Base URL:** `https://mindcloud.booqable.com/api/4`
- **Official documentation:** [Get New Order](https://developers.booqable.com/#orders-new-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields[orders]` | query | `string` | no | Comma-separated order fields to include instead of the default fields. |
| `include` | query | `string` | no | Comma-separated relationships to sideload. |
