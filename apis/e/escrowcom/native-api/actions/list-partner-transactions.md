# List Partner Transactions with Escrow.com

Retrieves partner transactions from Escrow.com.

## Endpoint

- **Method:** `GET`
- **Path:** `/partner/transactions`
- **Base URL:** `https://api.escrow-sandbox.com/2017-09-01`
- **Official documentation:** [List Partner Transactions](https://www.escrow.com/api/docs/reference)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum partner transactions to fetch. |
| `next_cursor` | query | `number` | no | Cursor to start fetching partner transactions from. |
| `sort_by` | query | `string` | no | Partner transaction sort field. |
| `sort_direction` | query | `string` | no | Sort direction, asc or desc. |
