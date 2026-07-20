# List Schedule Series By IDs with Avaza

Retrieves schedule series by IDs from Avaza.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/ScheduleSeries`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [List Schedule Series By IDs](https://api.avaza.com/#!/ScheduleSeries/ScheduleSeries_GetByFilter)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ScheduleSeriesIDs` | body | `list<number>` | yes |
| `UpdatedAfter` | body | `date` | no |
| `ScheduleStartDateFrom` | body | `date` | no |
| `ScheduleStartDateTo` | body | `date` | no |
| `ScheduleEndDateFrom` | body | `date` | no |
| `ScheduleEndDateTo` | body | `date` | no |
| `UserID` | body | `number` | no |
| `UserEmail` | body | `string` | no |
| `TimeSheetCategoryID` | body | `number` | no |
| `TimeSheetCategoryName` | body | `string` | no |
| `LeaveTypeID` | body | `number` | no |
| `ProjectID` | body | `number` | no |
| `CompanyID` | body | `number` | no |
| `PageSize` | body | `number` | no |
| `PageNumber` | body | `number` | no |
| `Sort` | body | `string` | no |
