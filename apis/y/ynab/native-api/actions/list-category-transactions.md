# List Category Transactions with YNAB

Retrieves transactions for a category in YNAB.

## Endpoint

- **Method:** `GET`
- **Path:** `/plans/:planId/categories/:categoryId/transactions`
- **Base URL:** `https://api.ynab.com/v1`
- **Official documentation:** [List Category Transactions](https://api.ynab.com/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `planId` | path | `string` | yes | The id of the plan. You can also use last-used or default when enabled. |
| `categoryId` | path | `string` | yes | The id of the category. |
| `sinceDate` | query | `date` | no | Only include transactions on or after this date. |
| `type` | query | `string` | no | Only include transactions of the specified type. |
| `lastKnowledgeOfServer` | query | `number` | no | Only include changes since this server knowledge value. |
