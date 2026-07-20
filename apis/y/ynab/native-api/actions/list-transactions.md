# List Transactions with YNAB

Retrieves transactions from a YNAB plan.

## Endpoint

- **Method:** `GET`
- **Path:** `/plans/:planId/transactions`
- **Base URL:** `https://api.ynab.com/v1`
- **Official documentation:** [List Transactions](https://api.ynab.com/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `planId` | path | `string` | yes | The id of the plan. You can also use last-used. |
| `since_date` | query | `date` | no | Only include transactions on or after this ISO date. |
| `type` | query | `string` | no | Filter to uncategorized or unapproved transactions. |
