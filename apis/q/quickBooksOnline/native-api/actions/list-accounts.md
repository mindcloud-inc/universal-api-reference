# List Accounts with QuickBooks Online

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://:quickbooksEnvironment/v3/company/:realmId`
- **Official documentation:** [List Accounts](https://developer.intuit.com/app/developer/qbo/docs/learn/explore-the-quickbooks-online-api/data-queries)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | QuickBooks SQL-like query. Add a WHERE clause to filter accounts, for example select * from Account where AccountType = 'Expense'. |
