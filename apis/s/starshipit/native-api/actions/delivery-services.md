# Delivery Services with Starshipit

## Endpoint

- **Method:** `POST`
- **Path:** `/deliveryservices`
- **Base URL:** `https://api.starshipit.com/api`
- **Official documentation:** [Delivery Services](https://api-docs.starshipit.com/#11419b42-fcda-4cf6-b5e4-d572ba69147f)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `order_id` | body | `number` | no |
| `refresh_rate` | body | `boolean` | no |
| `sender.street` | body | `string` | no |
| `sender.suburb` | body | `string` | no |
| `sender.city` | body | `string` | no |
| `sender.state` | body | `string` | no |
| `sender.post_code` | body | `string` | no |
| `sender.country_code` | body | `string` | no |
| `destination.street` | body | `string` | no |
| `destination.suburb` | body | `string` | no |
| `destination.city` | body | `string` | no |
| `destination.state` | body | `string` | no |
| `destination.post_code` | body | `string` | no |
| `destination.country_code` | body | `string` | no |
| `packages[]` | body | `array<object>` | no |
| `declared_value` | body | `number` | no |
| `return_order` | body | `boolean` | no |
| `include_pricing` | body | `boolean` | no |
| `signature_required` | body | `string` | no |
| `authority_to_leave` | body | `boolean` | no |
| `dangerous_goods` | body | `boolean` | no |
| `insurance_value` | body | `number` | no |
