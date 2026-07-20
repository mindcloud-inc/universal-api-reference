# List Account Transactions with YNAB

Retrieves transactions for an account in YNAB.

## Endpoint

- **Method:** `GET`
- **Path:** `/plans/:planId/accounts/:accountId/transactions`
- **Base URL:** `https://api.ynab.com/v1`
- **Official documentation:** [List Account Transactions](https://api.ynab.com/v1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `planId` | path | `string` | yes |
| `accountId` | path | `string` | yes |
| `since_date` | query | `date` | no |
| `type` | query | `string` | no |
| `last_knowledge_of_server` | query | `number` | no |
