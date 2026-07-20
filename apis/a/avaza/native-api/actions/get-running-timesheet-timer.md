# Get Running Timesheet Timer with Avaza

Retrieves the running timesheet timer from Avaza.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/TimesheetTimer`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [Get Running Timesheet Timer](https://api.avaza.com/#!/TimesheetTimer/TimesheetTimer_GetRunningTimer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `UserID` | query | `number` | no | Optional - User ID number if impersonating a different user. Otherwise assumes the current user. Only users with certain security roles have permission to impersonate other users |
