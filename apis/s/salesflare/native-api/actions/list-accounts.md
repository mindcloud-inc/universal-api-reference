# List Accounts with Salesflare

## Endpoint

- **Method:** `GET`
- **Path:** `accounts`
- **Base URL:** `https://api.salesflare.com`
- **Official documentation:** [List Accounts](https://api.salesflare.com/docs#/Accounts/getAccounts)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of accounts to return. |
| `order_by` | query | `string` | no | Sort expression such as name or creation_date desc. |
| `search` | query | `string` | no | Free-text search across accounts. |
| `offset` | query | `number` | no | Number of accounts to skip before returning results. |
