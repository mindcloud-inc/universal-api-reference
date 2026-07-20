# List Expense Merchants Lookup with Avaza

Retrieves expense merchants lookup entries from Avaza.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/ExpenseMerchant/Lookup`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [List Expense Merchants Lookup](https://api.avaza.com/#!/ExpenseMerchant/ExpenseMerchangeLookup)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search string to match against Expense Group Name |
