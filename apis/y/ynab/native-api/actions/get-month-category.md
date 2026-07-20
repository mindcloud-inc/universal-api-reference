# Get Month Category with YNAB

Retrieves a category for a specific month in YNAB.

## Endpoint

- **Method:** `GET`
- **Path:** `/plans/:planId/months/:month/categories/:categoryId`
- **Base URL:** `https://api.ynab.com/v1`
- **Official documentation:** [Get Month Category](https://api.ynab.com/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `planId` | path | `string` | yes | The id of the plan. You can also use last-used or default when enabled. |
| `month` | path | `string` | yes | The plan month in YYYY-MM-DD format or current. |
| `categoryId` | path | `string` | yes | The id of the category. |
