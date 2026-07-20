# Update Project with Avaza

Updates an existing project in Avaza.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/Project`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [Update Project](https://api.avaza.com/#!/Project/Project_Put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ProjectID` | body | `number` | no | The ID of the Project to update |
| `FieldsToUpdate` | body | `list<string>` | yes | — |
| `ProjectTitle` | body | `string` | no | (optional) An updated project title. (255 characters max) |
| `ProjectNotes` | body | `string` | no | (optional) Any descriptive notes about the project. (2000 characters max) |
| `TimesheetApprovalRequiredbyDefault` | body | `boolean` | no | Whether timesheet approval should be required by default for newly added project members. |
| `isTaskRequiredOnTimesheet` | body | `boolean` | no | Whether timesheets entered against this project require a task to be selected. |
| `StartDate` | body | `date` | no | — |
| `EndDate` | body | `date` | no | — |
| `BudgetAmount` | body | `number` | no | — |
| `BudgetHours` | body | `number` | no | — |
| `ProjectStatusCode` | body | `string` | no | Update the project status (string, optional): (Possible values: NotStarted, InProgress, Complete, OnHold) |
| `ProjectCategoryIDFK` | body | `number` | no | — |
| `ProjectBillableTypeCode` | body | `string` | no | The billing method of the project. (string, optional) Possible values: CategoryHourly, NoRate, NotBillable, PersonHourly, ProjectHourly |
| `ProjectBudgetTypeCode` | body | `string` | no | The project budgeting type. (string, optional) Possible values: NoBudget, PersonHours, ProjectFees, ProjectHours, CategoryHours |
