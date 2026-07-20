# List Money Movement Groups with YNAB

Retrieves money movement groups from a YNAB plan.

## Endpoint

- **Method:** `GET`
- **Path:** `/plans/:planId/money_movement_groups`
- **Base URL:** `https://api.ynab.com/v1`
- **Official documentation:** [List Money Movement Groups](https://api.ynab.com/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `planId` | path | `string` | yes | The id of the plan. You can also use last-used or default when enabled. |
