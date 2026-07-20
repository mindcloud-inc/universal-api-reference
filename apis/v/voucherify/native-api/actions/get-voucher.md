# Get Voucher with Voucherify

Retrieves a voucher from Voucherify by code or ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/vouchers/:voucherId`
- **Base URL:** `https://us1.api.voucherify.io/v1`
- **Official documentation:** [Get Voucher](https://docs.voucherify.io/reference/get-voucher)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `voucherId` | path | `string` | yes | Voucherify voucher identifier or code. |
