# List All Transfers with Column

## Endpoint

- **Method:** `GET`
- **Path:** `/transfers`
- **Base URL:** `https://api.column.com`
- **Official documentation:** [List All Transfers](https://column.com/docs/api/#transfer/list-all)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `string` | no | Transfer type filter; accepts comma-separated values. |
| `bank_account_id` | query | `string` | no | Filter transfers touching this bank account. |
| `counterparty_id` | query | `string` | no | Filter transfers associated with this counterparty. |
| `transfer_id` | query | `string` | no | Filter results to a specific transfer ID. |
| `status` | query | `string` | no | Filter by transfer status; accepts comma-separated values. |
| `is_incoming` | query | `boolean` | no | Whether to return incoming or outgoing transfers. |
