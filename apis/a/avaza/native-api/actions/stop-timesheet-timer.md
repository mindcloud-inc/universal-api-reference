# Stop Timesheet Timer with Avaza

Stops a running timesheet timer in Avaza.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/TimesheetTimer/:id`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [Stop Timesheet Timer](https://api.avaza.com/#!/TimesheetTimer/TimesheetTimer_StopTimer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The ID of the existing timesheet entry that needs its timer stopped |
| `UserID` | query | `number` | no | Optional - User ID number if impersonating a different user. Otherwise assumes the current user. Only users with certain security roles have permission to impersonate other users |
