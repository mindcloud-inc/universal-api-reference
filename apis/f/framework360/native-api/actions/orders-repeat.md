# Repeat Order with Framework360

## Endpoint

- **Method:** `POST`
- **Path:** `orders/repeat`
- **Base URL:** `https://mindcloudstage0.framework360.site/m/api`
- **Official documentation:** [Repeat Order](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Order ID to repeat. |
| `user_email` | body | `string` | yes | User email for the new order. |
| `cart[]` | body | `array<object>` | yes | Cart data to reuse for the new order. |
| `billing_data` | body | `object` | yes | Billing data for the repeated order. |
| `shipping_data` | body | `object` | yes | Shipping data for the repeated order. |
| `shipping_id` | body | `number` | no | Shipping method ID. |
| `order_status` | body | `number` | no | Initial status for the repeated order. |
| `payment_id` | body | `string` | no | Payment method ID. |
| `note` | body | `string` | no | Additional note for the repeated order. |
| `labels[]` | body | `array<string>` | no | Labels to assign to the repeated order. |
