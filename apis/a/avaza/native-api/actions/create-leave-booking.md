# Create Leave Booking with Avaza

Creates a leave booking in Avaza.

## Endpoint

- **Method:** `POST`
- **Path:** `/ScheduleSeries/AddLeave`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [Create Leave Booking](https://api.avaza.com/#!/ScheduleSeries/ScheduleSeries_AddLeave)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `LeaveUserIDFK` | body | `number` | no |
| `LeaveNotify` | body | `boolean` | no |
| `LeaveHoursPerDay` | body | `number` | no |
| `LeaveTypeIDFK` | body | `number` | no |
| `LeaveNotes` | body | `string` | no |
| `LeaveStartDate` | body | `date` | no |
| `LeaveEndDate` | body | `date` | no |
| `LeaveStartTime` | body | `string` | no |
