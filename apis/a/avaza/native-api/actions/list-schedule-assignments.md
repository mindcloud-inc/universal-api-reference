# List Schedule Assignments with Avaza

Retrieves schedule assignments from Avaza.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/ScheduleAssignment`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [List Schedule Assignments](https://api.avaza.com/#!/ScheduleAssignment/ScheduleAssignment_Get)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `UpdatedAfter` | query | `date` | no | Limit results to records updated after the specified date |
| `ScheduleDateFrom` | query | `date` | no | Filter for schedule assignement  that are  on or after a specific date |
| `ScheduleDateTo` | query | `date` | no | Filter for schedules that are on or before a specific date |
| `ScheduleSeriesID` | query | `number` | no | Filter to records for a particular Schedule Series |
| `UserID` | query | `number` | no | The UserID of a schedule user to filter assignments for. Only api users with Admin role can see all schedules across all users. Users with ScheduleUser role can access their own ScheduleSeries. |
| `UserEmail` | query | `string` | no | The email of the user who has been scheduled |
