# Validate Voucher with Vouchery.io

## Endpoint

- **Method:** `PUT`
- **Path:** `/vouchers/:code/validate`
- **Base URL:** `https://mindcloud.sandbox.vouchery.app/api/v2.1`
- **Official documentation:** [Validate Voucher](https://docs.vouchery.io/reference/putapiv21voucherscodevalidate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Voucher code |
| `additional_categories` | body | `object` | yes | Additional categories |
| `confirmed` | body | `boolean` | yes | Whether the redemption is confirmed |
| `product_items[]` | body | `array<object>` | no | Product items |
| `customer_identifier` | body | `string` | no | Customer identifier |
| `shipping_cost` | body | `number` | no | Shipping cost |
| `total_transaction_cost` | body | `number` | no | Total transaction cost |
| `transaction_id` | body | `string` | no | Transaction ID |
| `user_agent` | body | `string` | no | User agent |
