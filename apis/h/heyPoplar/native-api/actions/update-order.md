# Update Order with HeyPoplar

Updates an existing order in HeyPoplar.

## Endpoint

- **Method:** `POST`
- **Path:** `/order/:order_id`
- **Base URL:** `https://api.heypoplar.com/v1`
- **Official documentation:** [Update Order](https://docs.heypoplar.com/api/endpoints/orders#edit-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_id` | path | `string` | yes | The ID of the order to edit. |
| `order_date` | body | `string` | no | ISO8601 purchase date in YYYY-MM-DD format. |
| `customer_email` | body | `string` | no | Customer email address used to identify the order. |
| `total` | body | `number` | no | Updated order total. |
