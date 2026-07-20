# Submit Timesheets for Approval with Avaza

Submits timesheets for approval in Avaza.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/TimesheetSubmission`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [Submit Timesheets for Approval](https://api.avaza.com/#!/TimesheetSubmission/TimesheetSubmission_Post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `SendNotifications` | query | `boolean` | no | Send email alerts to timesheet approvers. Defaults to true |
| `WholeWeekOf` | query | `date` | no | A date (yyyy-MM-dd) that falls within  a Week to have all timesheets in that week submitted. Respects the First Day of Week setting in your account Timesheet Settings to determine the week range. |
| `WholeDayOf` | query | `date` | no | A date (yyyy-MM-dd) to submit all timesheets on this day |
| `UserID` | query | `number` | no | The user to submit timesheets for. Defaults to current user. Only allowed to be different from the current user when the current user has rights to Impersonate other users. |
