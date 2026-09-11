# Update Order with BigCommerce

Updates an Order

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/orders/:orderId`
- **Base URL:** `https://api.bigcommerce.com/stores/{storeHash}`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `status_id` | body | `string` | no |
| `orderId` | path | `string` | no |
| `customer_message` | body | `string` | no |
