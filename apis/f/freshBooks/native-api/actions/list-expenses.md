# List Expenses with FreshBooks

Retrieves expenses from FreshBooks for an account.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounting/account/:accountId/expenses/expenses`
- **Base URL:** `https://api.freshbooks.com`
- **Official documentation:** [List Expenses](https://www.freshbooks.com/api/expenses)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | FreshBooks accounting account ID. |
