# Get Time Tracking Record with BambooHR

Retrieves time tracking record from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/timetracking/record/:id`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Time Tracking Record](https://documentation.bamboohr.com/reference/get-time-tracking-record)

## Requirements

- **OAuth scopes:** `time_tracking`
- **scope:** `time_tracking` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The time tracking record ID used to originally create the record. |
