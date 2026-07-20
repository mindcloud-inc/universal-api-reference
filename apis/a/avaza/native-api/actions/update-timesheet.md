# Update Timesheet with Avaza

Updates an existing timesheet in Avaza.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/Timesheet`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [Update Timesheet](https://api.avaza.com/#!/Timesheet/Timesheet_Put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `TimeSheetEntryID` | body | `number` | yes | — |
| `FieldsToUpdate` | body | `list<string>` | yes | — |
| `ProjectIDFK` | body | `number` | yes | — |
| `TimesheetCategoryIDFK` | body | `number` | no | — |
| `TaskIDFK` | body | `number` | no | — |
| `Duration` | body | `number` | no | — |
| `EntryDate` | body | `date` | no | — |
| `hasStartEndTime` | body | `boolean` | no | — |
| `Notes` | body | `string` | no | — |
| `CustomMetadata` | body | `string` | no | Optional. free nvarchar field available via Api to store any additional metadata against a timesheet. We suggest you use Json or your preferred serialisation format. 1000 characters max. |
