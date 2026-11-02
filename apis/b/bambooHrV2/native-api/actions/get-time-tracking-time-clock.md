# Get Time Tracking Time Clock with BambooHR

Retrieves time tracking time clock from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-tracking/time-clocks/:id`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Time Tracking Time Clock](https://documentation.bamboohr.com/reference/get-time-tracking-time-clock)

## Requirements

- **OAuth scopes:** `time_tracking:time_clocks`
- **scope:** `time_tracking:time_clocks` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The time tracking time clock ID. |
