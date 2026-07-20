# List Accounts with YNAB

Retrieves accounts from a YNAB plan.

## Endpoint

- **Method:** `GET`
- **Path:** `/plans/:planId/accounts`
- **Base URL:** `https://api.ynab.com/v1`
- **Official documentation:** [List Accounts](https://api.ynab.com/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `planId` | path | `string` | yes | The id of the plan. You can also use last-used. |
| `last_knowledge_of_server` | query | `number` | no | Only include entities changed since this server knowledge value. |
