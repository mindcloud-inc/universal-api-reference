# Get Timesheet Summary with BambooHR

Retrieves timesheet summary from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-tracking/timesheets/:id/summary`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Timesheet Summary](https://documentation.bamboohr.com/reference/get-timesheet-summary)

## Requirements

- **OAuth scopes:** `time_tracking:timesheets`
- **scope:** `time_tracking:timesheets` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The timesheet ID. |
