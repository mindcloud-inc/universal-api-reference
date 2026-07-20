# List Money Movements with YNAB

Retrieves money movements from a YNAB plan.

## Endpoint

- **Method:** `GET`
- **Path:** `/plans/:planId/money_movements`
- **Base URL:** `https://api.ynab.com/v1`
- **Official documentation:** [List Money Movements](https://api.ynab.com/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `planId` | path | `string` | yes | The id of the plan. You can also use last-used or default when enabled. |
