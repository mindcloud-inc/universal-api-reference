# Get Timesheet Data with AssessTEAM

Retrieves recorded timesheet data from AssessTEAM.

## Endpoint

- **Method:** `GET`
- **Path:** `/timesheet/gettimesheetdata`
- **Base URL:** `https://restapi.assessteam.com`
- **Official documentation:** [Get Timesheet Data](https://restapi.assessteam.com/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `month` | query | `string` | yes | Month, for example Apr-2026. |
| `personcode` | query | `string` | yes | Unique person code, for example 1001. |
| `projectname` | query | `string` | no | Project name to narrow the result. |
| `date` | query | `string` | no | Date for day mode, for example 5-Mar-2025. |
| `daywisetimesheet` | query | `boolean` | no | Show day-wise timesheet data when true. |
| `projectwisetiesheet` | query | `boolean` | no | Show project-wise timesheet data with comments when true. |
