# List Expenses with LimoExpress

Retrieves expenses from the LimoExpress organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/integration/expenses`
- **Base URL:** `https://api.limoexpress.me`
- **Official documentation:** [List Expenses](https://api.limoexpress.me/api/docs/v1#/Expenses/getAllExpenses)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_string` | query | `string` | no | Search across expense fields. |
| `page` | query | `number` | no | Page number, default is 1. |
| `per_page` | query | `number` | no | Items per page, default is 20. |
