# List Schedule Series with Avaza

Retrieves schedule series from Avaza.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/ScheduleSeries`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [List Schedule Series](https://api.avaza.com/#!/ScheduleSeries/ScheduleSeries_Get)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `UpdatedAfter` | query | `date` | no | Limit results to records updated after the specified date |
| `ScheduleStartDateFrom` | query | `date` | no | Filter for schedules that start on or after a specific date |
| `ScheduleStartDateTo` | query | `date` | no | Filter for schedules that start on or before a specific date |
| `ScheduleEndDateFrom` | query | `date` | no | Filter for schedules that end on or after a specific date |
| `ScheduleEndDateTo` | query | `date` | no | Filter for schedules that end on or before a specific date |
| `UserID` | query | `number` | no | The UserID of a schedule user to filter assignments for. Only api users with Admin role can see all schedules across all users. Users with ScheduleUser role can access their own ScheduleSeries. |
| `UserEmail` | query | `string` | no | The email of the user who has been scheduled |
| `TimeSheetCategoryID` | query | `number` | no | Filter for schedule records linked to a specific timesheeet category |
| `TimeSheetCategoryName` | query | `string` | no | Filter for schedule records with a specific timesheeet category name (exact string match) |
| `LeaveTypeID` | query | `number` | no | Filter to records of a particular leave type |
| `ProjectID` | query | `number` | no | Filter to only include books linked to a specific project |
| `CompanyID` | query | `number` | no | Filter to only include records linked to projects, where that project belongs to a specific customer company |
