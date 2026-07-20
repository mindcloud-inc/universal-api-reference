# Create Order with Framework360

## Endpoint

- **Method:** `POST`
- **Path:** `orders/create`
- **Base URL:** `https://mindcloudstage0.framework360.site/m/api`
- **Official documentation:** [Create Order](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_email` | body | `string` | yes | Email of the user placing the order. |
| `cart[]` | body | `array<object>` | yes | Items included in the order cart. |
| `billing_data` | body | `object` | yes | Billing data for the order. |
| `shipping_data` | body | `object` | yes | Shipping data for the order. |
| `shipping_id` | body | `number` | no | Shipping method ID. |
| `order_status` | body | `number` | no | Initial order status. |
| `payment_id` | body | `string` | no | Payment method ID. |
| `labels[]` | body | `array<string>` | no | Labels to assign to the order. |
| `note` | body | `string` | no | Additional order notes. |
