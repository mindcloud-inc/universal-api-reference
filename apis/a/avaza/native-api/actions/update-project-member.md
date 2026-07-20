# Update Project Member with Avaza

Updates an existing project member in Avaza.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/ProjectMember`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [Update Project Member](https://api.avaza.com/#!/ProjectMember/ProjectMember_Put)

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
| `ProjectIDFK` | body | `number` | yes | Required. The ProjectID |
| `UserIDFK` | body | `number` | yes | Required. The UserID |
| `FieldsToUpdate` | body | `list<string>` | yes | A string array of field names to be updated. |
| `CostAmount` | body | `number` | no | A new Cost Amount. Defaults to null. |
| `RateAmount` | body | `number` | no | A new Rate Amount. Defaults to null. |
| `BudgetAmount` | body | `number` | no | A new Budget Amount. Defaults to null. |
