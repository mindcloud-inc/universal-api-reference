# Update Timesheet with Craftboxx

Updates a timesheet in Craftboxx.

## Endpoint

- **Method:** `PUT`
- **Path:** `timesheets/:timesheetId`
- **Base URL:** `https://api.craftboxx.de`
- **Official documentation:** [Update Timesheet](https://api.craftboxx.de/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end` | body | `string` | no | The timesheet end date or timestamp. |
| `start` | body | `string` | no | The timesheet start date or timestamp. |
| `timesheetId` | path | `number` | yes | The Craftboxx timesheet ID. |
| `working_time` | body | `number` | no | The working time in minutes. |
| `break_time` | body | `number` | no | The break time in minutes. |
