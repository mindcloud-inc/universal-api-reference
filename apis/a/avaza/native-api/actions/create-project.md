# Create Project with Avaza

Creates a new project in Avaza.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/Project`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [Create Project](https://api.avaza.com/#!/Project/Project_Post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CompanyIDFK` | body | `number` | no | An ID of a company in Avaza to create the Project under. You must provide either a CompanyID, or a CompanyName |
| `CompanyName` | body | `string` | no | The name for a Company to create the project under. Will create company unless it matches an existing company name |
| `CurrencyCode` | body | `string` | no | The ISO 3 letter currency code to use when creating a new Company. If not provided, the account's default currency will be used. |
| `ProjectTitle` | body | `string` | yes | The title of the new project. (255 characters max) |
| `ProjectCode` | body | `string` | no | Used when Manual Project Codes are enabled |
| `ProjectNotes` | body | `string` | no | Any descriptive notes about the project. (2000 characters max) |
| `TimesheetApprovalRequiredbyDefault` | body | `boolean` | no | — |
| `PopulateDefaultProjectMembers` | body | `boolean` | no | Defaults to true. |
| `isTaskRequiredOnTimesheet` | body | `boolean` | no | — |
| `StartDate` | body | `date` | no | — |
| `EndDate` | body | `date` | no | — |
| `BudgetAmount` | body | `number` | no | — |
| `BudgetHours` | body | `number` | no | — |
| `ProjectStatusCode` | body | `string` | no | — |
| `ProjectCategoryIDFK` | body | `number` | no | — |
