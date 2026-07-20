# Update Voucher with Voucherify

Updates an existing voucher in Voucherify.

## Endpoint

- **Method:** `PUT`
- **Path:** `/vouchers/:voucherId`
- **Base URL:** `https://us1.api.voucherify.io/v1`
- **Official documentation:** [Update Voucher](https://docs.voucherify.io/api-reference/vouchers)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `metadata` | body | `object` | no |
| `voucherId` | path | `string` | yes |
