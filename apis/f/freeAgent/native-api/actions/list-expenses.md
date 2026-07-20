# List Expenses with FreeAgent

Retrieves a list of expenses from FreeAgent.

## Endpoint

- **Method:** `GET`
- **Path:** `/expenses`
- **Base URL:** `https://api.freeagent.com/v2`
- **Official documentation:** [List Expenses](https://dev.freeagent.com/docs/expenses#list-all-expenses)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `updated_since` | query | `date` | no | Only return expenses updated after this timestamp. |
| `view` | query | `string` | no | Filter the expense collection by FreeAgent view. |
