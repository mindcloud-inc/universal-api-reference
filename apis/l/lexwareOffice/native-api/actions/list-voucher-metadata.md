# List Voucher Metadata with Lexware Office

Retrieves and filters voucher metadata in Lexware Office.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/voucherlist`
- **Base URL:** `https://api.lexware.io`
- **Official documentation:** [List Voucher Metadata](https://developers.lexware.io/docs/#voucherlist-endpoint-retrieve-and-filter-voucherlist)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `voucherType` | query | `string` | yes | Comma-separated voucher types or any. |
| `voucherStatus` | query | `string` | yes | Comma-separated voucher statuses or any. |
| `archived` | query | `boolean` | no | Filter archived vouchers. |
| `contactId` | query | `string` | no | Existing Lexware contact ID. |
| `voucherDateFrom` | query | `date` | no | Filter by voucher date from yyyy-MM-dd. |
| `voucherDateTo` | query | `date` | no | Filter by voucher date to yyyy-MM-dd. |
| `createdDateFrom` | query | `date` | no | Filter by created date from yyyy-MM-dd. |
| `createdDateTo` | query | `date` | no | Filter by created date to yyyy-MM-dd. |
| `updatedDateFrom` | query | `date` | no | Filter by updated date from yyyy-MM-dd. |
| `updatedDateTo` | query | `date` | no | Filter by updated date to yyyy-MM-dd. |
| `voucherNumber` | query | `string` | no | Exact voucher number filter. |
