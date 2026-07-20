# Update Leave Booking with Avaza

Updates an existing leave booking in Avaza.

## Endpoint

- **Method:** `PUT`
- **Path:** `/ScheduleSeries/EditLeave`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [Update Leave Booking](https://api.avaza.com/#!/ScheduleSeries/ScheduleSeries_EditLeave)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ScheduleSeriesID` | body | `number` | no |
| `UserIDFK` | body | `number` | no |
| `HoursPerDay` | body | `number` | no |
| `LeaveTypeIDFK` | body | `number` | no |
| `Notes` | body | `string` | no |
| `StartDate` | body | `date` | no |
| `EndDate` | body | `date` | no |
| `StartTime` | body | `string` | no |
