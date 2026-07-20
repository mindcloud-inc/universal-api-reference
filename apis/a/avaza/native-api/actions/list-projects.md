# List Projects with Avaza

Retrieves projects from Avaza.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/Project`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [List Projects](https://api.avaza.com/#!/Project/Project_Get)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `UpdatedAfter` | query | `date` | no | Only show project records updated after a certain date (UTC) |
| `TimesheetUserID` | query | `number` | no | Filter to the projects that the supplied UserID can add timesheets to |
| `CompanyID` | query | `number` | no | — |
| `ProjectCategoryID` | query | `number` | no | — |
| `ProjectOwnerUserID` | query | `number` | no | — |
| `ProjectStatusCode` | query | `string` | no | — |
| `ProjectBillableTypeCode` | query | `string` | no | — |
| `ProjectBudgetTypeCode` | query | `string` | no | — |
| `DateCreatedFrom` | query | `date` | no | — |
| `DateCreatedTo` | query | `date` | no | — |
| `includeArchived` | query | `boolean` | no | Include Archived Projects in the results |
