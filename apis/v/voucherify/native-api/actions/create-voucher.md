# Create Voucher with Voucherify

Creates a new voucher in Voucherify.

## Endpoint

- **Method:** `POST`
- **Path:** `/vouchers`
- **Base URL:** `https://us1.api.voucherify.io/v1`
- **Official documentation:** [Create Voucher](https://docs.voucherify.io/api-reference/vouchers)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `code` | body | `string` | yes |
| `discount.amount_off` | body | `number` | yes |
| `discount.type` | body | `string` | yes |
| `type` | body | `string` | yes |
