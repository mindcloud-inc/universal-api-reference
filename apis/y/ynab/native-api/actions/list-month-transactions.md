# List Month Transactions with YNAB

Retrieves transactions for a month in YNAB.

## Endpoint

- **Method:** `GET`
- **Path:** `/plans/:planId/months/:month/transactions`
- **Base URL:** `https://api.ynab.com/v1`
- **Official documentation:** [List Month Transactions](https://api.ynab.com/v1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `planId` | path | `string` | yes |
| `month` | path | `string` | yes |
| `since_date` | query | `date` | no |
| `type` | query | `string` | no |
| `last_knowledge_of_server` | query | `number` | no |
