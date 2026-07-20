# List Payee Transactions with YNAB

Retrieves transactions for a payee in YNAB.

## Endpoint

- **Method:** `GET`
- **Path:** `/plans/:planId/payees/:payeeId/transactions`
- **Base URL:** `https://api.ynab.com/v1`
- **Official documentation:** [List Payee Transactions](https://api.ynab.com/v1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `planId` | path | `string` | yes |
| `payeeId` | path | `string` | yes |
| `since_date` | query | `date` | no |
| `type` | query | `string` | no |
| `last_knowledge_of_server` | query | `number` | no |
