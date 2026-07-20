# Create Timesheet with Avaza

Creates a new timesheet in Avaza.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/Timesheet`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [Create Timesheet](https://api.avaza.com/#!/Timesheet/Timesheet_Post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `UserIDFK` | body | `number` | no | UserID for a Timesheet user in Avaza |
| `ProjectIDFK` | body | `number` | no | The project to associate the timesheet with. |
| `TimesheetCategoryIDFK` | body | `number` | no | The Project timesheet category to link the timesheet to |
| `Duration` | body | `number` | no | The duration of the timesheet, in decimal hours. If null or 0, a timer will be started. |
| `isInvoiced` | body | `boolean` | no | Optional. False by default. Allows you to mark the timesheet as invoiced in an external system. |
| `EntryDate` | body | `date` | no | The date of the timesheet entry, with an optional start time component. |
| `hasStartEndTime` | body | `boolean` | no | If true, the start time will be take from the time component of the Entry Date field, and the end time will be calculated by adding the Duration to the StartDate |
| `Notes` | body | `string` | no | Timesheet Notes |
| `TaskIDFK` | body | `number` | no | Optional. Link the timesheet to a specific task |
| `CustomMetadata` | body | `string` | no | Optional. free nvarchar field available via Api to store any additional metadata against a timesheet. We suggest you use Json or your preferred serialisation format. 1000 characters max. |
