# Get Timely Timesheet Data with AssessTEAM

Retrieves timely timesheet data from AssessTEAM.

## Endpoint

- **Method:** `GET`
- **Path:** `/timesheet/getTimelyTimesheetData`
- **Base URL:** `https://restapi.assessteam.com`
- **Official documentation:** [Get Timely Timesheet Data](https://restapi.assessteam.com/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `month` | query | `string` | yes | Month, for example Apr-2026. |
| `daywisetimesheet` | query | `boolean` | no | Show day-wise timesheet data when true. |
