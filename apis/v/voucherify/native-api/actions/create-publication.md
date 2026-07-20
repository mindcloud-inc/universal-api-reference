# Create Publication with Voucherify

Creates a publication in Voucherify for eligible vouchers.

## Endpoint

- **Method:** `POST`
- **Path:** `/publications`
- **Base URL:** `https://us1.api.voucherify.io/v1`
- **Official documentation:** [Create Publication](https://docs.voucherify.io/api-reference/publications)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customer` | body | `string` | yes |
| `voucher` | body | `string` | yes |
