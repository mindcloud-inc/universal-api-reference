# List Voucher Transactions with Voucherify

Retrieves a voucher's transactions from Voucherify.

## Endpoint

- **Method:** `GET`
- **Path:** `/vouchers/:voucherId/transactions`
- **Base URL:** `https://us1.api.voucherify.io/v1`
- **Official documentation:** [List Voucher Transactions](https://docs.voucherify.io/api-reference/vouchers/list-voucher-transactions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `voucherId` | path | `string` | yes | Voucherify voucher identifier or code. |
