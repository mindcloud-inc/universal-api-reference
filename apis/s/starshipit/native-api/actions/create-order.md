# Create Order with Starshipit

## Endpoint

- **Method:** `POST`
- **Path:** `/orders`
- **Base URL:** `https://api.starshipit.com/api`
- **Official documentation:** [Create Order](https://api-docs.starshipit.com/#abcadf5c-9793-47b3-a2cb-d650c666d84d)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `order.order_date` | body | `date` | no |
| `order.order_number` | body | `string` | no |
| `order.reference` | body | `string` | no |
| `order.carrier` | body | `string` | no |
| `order.carrier_name` | body | `string` | no |
| `order.shipping_method` | body | `string` | no |
| `order.signature_required` | body | `boolean` | no |
| `order.return_order` | body | `boolean` | no |
| `order.destination.name` | body | `string` | no |
| `order.destination.phone` | body | `string` | no |
| `order.destination.street` | body | `string` | no |
| `order.destination.suburb` | body | `string` | no |
| `order.destination.state` | body | `string` | no |
| `order.destination.post_code` | body | `string` | no |
| `order.destination.country` | body | `string` | no |
| `order.destination.delivery_instructions` | body | `string` | no |
| `order.items[]` | body | `array<object>` | no |
