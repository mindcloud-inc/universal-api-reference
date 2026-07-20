# Update Project Timesheet Category with Avaza

Updates an existing project timesheet category in Avaza.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/ProjectTimesheetCategory`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [Update Project Timesheet Category](https://api.avaza.com/#!/ProjectTimesheetCategory/ProjectTimesheetCategory_Put)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ProjectIDFK` | body | `number` | no |
| `TimesheetCategoryIDFK` | body | `number` | no |
| `isBillable` | body | `boolean` | no |
| `isPayable` | body | `boolean` | no |
| `RateAmount` | body | `number` | no |
| `BudgetHours` | body | `number` | no |
| `CostAmount` | body | `number` | no |
