# List Transactions with Stax

Retrieves transactions from Stax.

## Endpoint

- **Method:** `GET`
- **Path:** `/transaction`
- **Base URL:** `https://apiprod.fattlabs.com`
- **Official documentation:** [List Transactions](https://docs.staxpayments.com/reference/list-and-filter-all-transactions)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `direction` | query | `string` | no | Sort direction. |
| `page` | query | `string` | no | Page number for paginated transaction results. |
| `sort` | query | `string` | no | Transaction sort field. |
| `status` | query | `string` | no | Transaction status selector. |
