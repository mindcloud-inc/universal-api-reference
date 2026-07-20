# List Book Transfers with Column

## Endpoint

- **Method:** `GET`
- **Path:** `/transfers/book`
- **Base URL:** `https://api.column.com`
- **Official documentation:** [List Book Transfers](https://column.com/docs/api/#book-transfer/list-all)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sender_bank_account_id` | query | `string` | no | Filter book transfers by sender bank account. |
| `receiver_bank_account_id` | query | `string` | no | Filter book transfers by receiver bank account. |
| `status` | query | `string` | no | Filter book transfers by status. |
