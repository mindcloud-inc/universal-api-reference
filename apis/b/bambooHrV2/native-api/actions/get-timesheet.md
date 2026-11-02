# Get Timesheet with BambooHR

Retrieves timesheet from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-tracking/timesheets/:id`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Timesheet](https://documentation.bamboohr.com/reference/get-timesheet)

## Requirements

- **OAuth scopes:** `time_tracking:timesheets`
- **scope:** `time_tracking:timesheets` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The timesheet ID. |
