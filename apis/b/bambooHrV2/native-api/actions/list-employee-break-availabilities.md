# List Employee Break Availabilities with BambooHR

Lists employee break availabilities from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-tracking/employees/:id/break-availabilities`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Employee Break Availabilities](https://documentation.bamboohr.com/reference/list-employee-break-availabilities)

## Requirements

- **OAuth scopes:** `time_tracking:breaks`
- **scope:** `time_tracking:breaks` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The internal employee ID. |
| `effective` | query | `string` | no | The employee's local time that should be used to calculate availability. Defaults to the current time. Must be in Y-m-d\TH:i:s format (no timezone offset). |
