# Create Redemption with Vouchery.io

## Endpoint

- **Method:** `POST`
- **Path:** `/vouchers/:code/redemptions`
- **Base URL:** `https://mindcloud.sandbox.vouchery.app/api/v2.1`
- **Official documentation:** [Create Redemption](https://docs.vouchery.io/reference/postapiv21voucherscoderedemptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Voucher code from the path. |
| `additional_categories` | body | `object` | yes | Additional redemption categories object. |
| `confirmed` | body | `boolean` | yes | Whether the redemption is confirmed immediately. |
| `product_items[]` | body | `array<object>` | no | Purchased product items. |
| `customer_identifier` | body | `string` | no | Customer identifier in your system. |
| `shipping_cost` | body | `number` | no | Shipping cost. |
| `total_transaction_cost` | body | `number` | no | Total transaction cost excluding shipping. |
| `transaction_id` | body | `string` | no | Underlying transaction identifier. |
| `user_agent` | body | `string` | no | User agent string. |
