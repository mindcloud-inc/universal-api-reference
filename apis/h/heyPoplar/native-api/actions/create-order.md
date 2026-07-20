# Create Order with HeyPoplar

Creates a new order in HeyPoplar.

## Endpoint

- **Method:** `POST`
- **Path:** `/order`
- **Base URL:** `https://api.heypoplar.com/v1`
- **Official documentation:** [Create Order](https://docs.heypoplar.com/api/endpoints/orders#submit-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_id` | body | `string` | yes | The unique identifier for this order. |
| `order_date` | body | `string` | yes | ISO8601 purchase date in YYYY-MM-DD format. |
| `customer_email` | body | `string` | yes | Customer email address. Poplar hashes it and discards the plaintext value. |
| `total` | body | `number` | no | Total order value as a decimal number. |
