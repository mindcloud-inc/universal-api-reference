# List Wire Transfers with Column

## Endpoint

- **Method:** `GET`
- **Path:** `/transfers/wire`
- **Base URL:** `https://api.column.com`
- **Official documentation:** [List Wire Transfers](https://column.com/docs/api/#wire-transfer/list-all)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bank_account_id` | query | `string` | no | Filter wire transfers associated with this bank account. |
| `counterparty_id` | query | `string` | no | Filter wire transfers associated with this counterparty. |
| `status` | query | `string` | no | Filter wire transfers by status. |
| `is_incoming` | query | `boolean` | no | Whether to return incoming or outgoing wire transfers. |
