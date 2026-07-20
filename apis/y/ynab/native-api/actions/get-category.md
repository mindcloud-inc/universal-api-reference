# Get Category with YNAB

Retrieves a category from a YNAB plan.

## Endpoint

- **Method:** `GET`
- **Path:** `/plans/:planId/categories/:categoryId`
- **Base URL:** `https://api.ynab.com/v1`
- **Official documentation:** [Get Category](https://api.ynab.com/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `planId` | path | `string` | yes | The id of the plan. You can also use last-used. |
| `categoryId` | path | `string` | yes | The id of the category. |
