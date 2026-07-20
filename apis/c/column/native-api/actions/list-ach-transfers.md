# List ACH Transfers with Column

## Endpoint

- **Method:** `GET`
- **Path:** `/transfers/ach`
- **Base URL:** `https://api.column.com`
- **Official documentation:** [List ACH Transfers](https://column.com/docs/api/#ach-transfer/list-all)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bank_account_id` | query | `string` | no | Filter ACH transfers associated with this bank account. |
| `counterparty_id` | query | `string` | no | Filter ACH transfers associated with this counterparty. |
| `status` | query | `string` | no | Filter ACH transfers by status. |
| `is_incoming` | query | `boolean` | no | Whether to return incoming or outgoing ACH transfers. |
| `type` | query | `string` | no | ACH transfer direction filter: CREDIT or DEBIT. |
