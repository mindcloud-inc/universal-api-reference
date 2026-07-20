# Update Order with Starshipit

## Endpoint

- **Method:** `PUT`
- **Path:** `/orders`
- **Base URL:** `https://api.starshipit.com/api`
- **Official documentation:** [Update Order](https://api-docs.starshipit.com/#fffefde7-2198-4e38-ae33-283792fd8321)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `order.order_id` | body | `number` | no |
| `order.order_date` | body | `date` | no |
| `order.order_number` | body | `string` | no |
| `order.reference` | body | `string` | no |
| `order.carrier` | body | `string` | no |
| `order.carrier_service_code` | body | `string` | no |
| `order.shipping_method` | body | `string` | no |
| `order.signature_required` | body | `boolean` | no |
| `order.destination.name` | body | `string` | no |
| `order.destination.phone` | body | `string` | no |
| `order.destination.street` | body | `string` | no |
| `order.destination.suburb` | body | `string` | no |
| `order.destination.state` | body | `string` | no |
| `order.destination.post_code` | body | `string` | no |
| `order.destination.country` | body | `string` | no |
| `order.destination.delivery_instructions` | body | `string` | no |
| `order.items[]` | body | `array<object>` | no |
| `order.packages[]` | body | `array<object>` | no |
