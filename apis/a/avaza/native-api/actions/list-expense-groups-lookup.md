# List Expense Groups Lookup with Avaza

Retrieves expense groups lookup entries from Avaza.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/ExpenseGroup/Lookup`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [List Expense Groups Lookup](https://api.avaza.com/#!/ExpenseGroup/ExpenseGroupLookup)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search string to match against Expense Group Name |
