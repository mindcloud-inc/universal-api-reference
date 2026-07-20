# Create Project Timesheet Category with Avaza

Creates a new project timesheet category in Avaza.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/ProjectTimesheetCategory`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [Create Project Timesheet Category](https://api.avaza.com/#!/ProjectTimesheetCategory/ProjectTimesheetCategory_Post)

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
