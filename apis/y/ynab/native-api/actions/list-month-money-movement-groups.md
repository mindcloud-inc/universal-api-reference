# List Month Money Movement Groups with YNAB

Retrieves money movement groups for a month in YNAB.

## Endpoint

- **Method:** `GET`
- **Path:** `/plans/:planId/months/:month/money_movement_groups`
- **Base URL:** `https://api.ynab.com/v1`
- **Official documentation:** [List Month Money Movement Groups](https://api.ynab.com/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `planId` | path | `string` | yes | The id of the plan. You can also use last-used or default when enabled. |
| `month` | path | `string` | yes | The plan month in YYYY-MM-DD format or current. |
