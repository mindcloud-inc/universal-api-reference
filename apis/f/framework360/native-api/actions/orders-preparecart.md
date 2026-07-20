# Prepare Order with Framework360

## Endpoint

- **Method:** `POST`
- **Path:** `orders/prepareCart`
- **Base URL:** `https://mindcloudstage0.framework360.site/m/api`
- **Official documentation:** [Prepare Order](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cart[]` | body | `array<object>` | yes | Items to add to the cart. |
| `customer_id` | body | `number` | no | Customer ID for the cart preparation. |
| `shipping_id` | body | `number` | no | Shipping method ID. |
| `payment_id` | body | `number` | no | Payment method ID. |
