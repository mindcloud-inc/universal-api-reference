# Create Timesheet with Craftboxx

Creates a timesheet in Craftboxx.

## Endpoint

- **Method:** `POST`
- **Path:** `timesheets`
- **Base URL:** `https://api.craftboxx.de`
- **Official documentation:** [Create Timesheet](https://api.craftboxx.de/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employee_id` | body | `number` | yes | The employee ID for the timesheet. |
| `end` | body | `string` | no | The timesheet end date or timestamp. |
| `start` | body | `string` | no | The timesheet start date or timestamp. |
| `working_time` | body | `number` | no | The working time in minutes. |
| `break_time` | body | `number` | no | The break time in minutes. |
