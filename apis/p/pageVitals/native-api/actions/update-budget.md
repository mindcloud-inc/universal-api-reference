# Update Budget with PageVitals

## Endpoint

- **Method:** `PUT`
- **Path:** `/:websiteId/budgets/:budgetId`
- **Base URL:** `https://api.pagevitals.com`
- **Official documentation:** [Update Budget](https://pagevitals.com/docs/rest-api/reference/budgets/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `websiteId` | path | `string` | yes |
| `budgetId` | path | `string` | yes |
| `metric` | body | `string` | yes |
| `operator` | body | `string` | yes |
| `value` | body | `string` | yes |
| `device` | body | `string` | yes |
