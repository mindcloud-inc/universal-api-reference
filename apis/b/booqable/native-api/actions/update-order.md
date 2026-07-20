# Update Order with Booqable

Updates an existing order in Booqable.

## Endpoint

- **Method:** `PUT`
- **Path:** `/orders/:id`
- **Base URL:** `https://mindcloud.booqable.com/api/4`
- **Official documentation:** [Update Order](https://developers.booqable.com/#orders-update-an-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The UUID of the order to update. |
| `data` | body | `object` | yes | JSON:API order payload with the nested `data` object expected by Booqable. Include the order id, type, and any attributes or relationships you want to update. |
| `fields[orders]` | query | `string` | no | Comma-separated order fields to include instead of the default fields. |
| `include` | query | `string` | no | Comma-separated relationships to sideload. |
