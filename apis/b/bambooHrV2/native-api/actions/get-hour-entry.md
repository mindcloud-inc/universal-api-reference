# Get Hour Entry with BambooHR

Retrieves hour entry from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-tracking/hour-entries/:id`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Hour Entry](https://documentation.bamboohr.com/reference/get-hour-entry)

## Requirements

- **OAuth scopes:** `time_tracking:timesheets`
- **scope:** `time_tracking:timesheets` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The hour entry ID. |
