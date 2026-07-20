# Start Timesheet Timer with Avaza

Starts a timesheet timer in Avaza.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/TimesheetTimer/:id`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [Start Timesheet Timer](https://api.avaza.com/#!/TimesheetTimer/TimesheetTimer_StartTimer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | id of timesheet entry that should be used as the basis for running a timer. If the existing timesheet is not on the current day, or you have start/end times enabled, then a new timesheet will be created for the timer. |
| `UserID` | query | `number` | no | Optional - User ID number if impersonating a different user. Otherwise assumes the current user. Only users with certain security roles have permission to impersonate other users |
