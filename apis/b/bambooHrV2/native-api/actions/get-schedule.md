# Get Schedule with BambooHR

Retrieves schedule from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/scheduling/schedules/:id`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Schedule](https://documentation.bamboohr.com/reference/scheduling-get-schedule)

## Requirements

- **OAuth scopes:** `scheduling:schedules time_tracking`
- **scope:** `scheduling:schedules, time_tracking` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the schedule |
