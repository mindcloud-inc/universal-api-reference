# Get Month with YNAB

Retrieves a month from a YNAB plan.

## Endpoint

- **Method:** `GET`
- **Path:** `/plans/:planId/months/:month`
- **Base URL:** `https://api.ynab.com/v1`
- **Official documentation:** [Get Month](https://api.ynab.com/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `planId` | path | `string` | yes | The id of the plan. You can also use last-used. |
| `month` | path | `string` | yes | The budget month in YYYY-MM-DD format. |
