# List Expense Categories with FreshBooks

Retrieves expense categories from FreshBooks for an account.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounting/account/:accountId/expenses/categories`
- **Base URL:** `https://api.freshbooks.com`
- **Official documentation:** [List Expense Categories](https://www.freshbooks.com/api/expenses)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | FreshBooks account ID from the authenticated business context. |
