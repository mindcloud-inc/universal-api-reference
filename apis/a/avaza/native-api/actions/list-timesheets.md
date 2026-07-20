# List Timesheets with Avaza

Retrieves timesheets from Avaza.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/Timesheet`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [List Timesheets](https://api.avaza.com/#!/Timesheet/Timesheet_Get)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `UpdatedAfter` | query | `date` | no | — |
| `EntryDateFrom` | query | `date` | no | — |
| `EntryDateTo` | query | `date` | no | — |
| `UserID` | query | `number` | no | The UserID of a timesheet user to filter timesheets for. Only api users with certain higher roles can see timesheets across multiple users. |
| `UserEmail` | query | `string` | no | — |
| `CategoryName` | query | `string` | no | — |
| `TimesheetEntryApprovalStatusCode` | query | `string` | no | — |
| `ProjectID` | query | `number` | no | — |
| `TaskID` | query | `number` | no | — |
| `isBillable` | query | `boolean` | no | — |
| `isInvoiced` | query | `boolean` | no | — |
| `isTimerRunning` | query | `boolean` | no | — |
| `includeInvoiceDetails` | query | `boolean` | no | Defaults to false. When true, the InvoiceIDFK value will be included in the response. |
