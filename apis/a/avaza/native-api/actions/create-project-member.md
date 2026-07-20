# Create Project Member with Avaza

Creates a new project member in Avaza.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/ProjectMember`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [Create Project Member](https://api.avaza.com/#!/ProjectMember/ProjectMember_Post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `isTimesheetAllowed` | body | `boolean` | no | — |
| `isTimesheetApprover` | body | `boolean` | no | — |
| `isExpenseApprover` | body | `boolean` | no | — |
| `isTimesheetApprovalRequired` | body | `boolean` | no | — |
| `canCreateTasks` | body | `boolean` | no | — |
| `canDeleteTasks` | body | `boolean` | no | — |
| `canCommentOnTasks` | body | `boolean` | no | — |
| `canUpdateTasks` | body | `boolean` | no | — |
| `ProjectIDFK` | body | `number` | no | Required. The ProjectID |
| `UserIDFK` | body | `number` | no | Required. The UserID to assign |
| `CostAmount` | body | `number` | no | Optional. If not provided, defaults to the User's default Cost Amount. |
| `RateAmount` | body | `number` | no | Optional. If not provided, defaults to the User's default Rate Amount. |
| `BudgetAmount` | body | `number` | no | Optional |
