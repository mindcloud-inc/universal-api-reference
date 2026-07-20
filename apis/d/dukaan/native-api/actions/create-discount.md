# Create Discount with Dukaan

Creates a new discount in Dukaan.

## Endpoint

- **Method:** `POST`
- **Path:** `api/coupon/seller/coupon/v2/`
- **Base URL:** `https://api.mydukaan.io`
- **Official documentation:** [Create Discount](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | body | `string` | yes | Discount code. |
| `discount_value` | body | `string` | yes | Discount value. |
| `min_order_value` | body | `string` | no | Minimum order value. |
| `discount_type` | body | `number` | no | Dukaan discount type code. |
| `auto_apply` | body | `boolean` | no | Whether Dukaan should auto-apply the coupon. |
| `is_active` | body | `boolean` | no | Whether the discount is active. |
| `start_date` | body | `date` | no | Discount start date/time. |
| `expiry_date` | body | `date` | no | Discount expiry date/time. |
| `max_discount` | body | `string` | no | Maximum discount amount. |
