# Get Time Tracking Import with BambooHR

Retrieves time tracking import from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-tracking/imports/:id`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Time Tracking Import](https://documentation.bamboohr.com/reference/get-time-tracking-import)

## Requirements

- **OAuth scopes:** `time_tracking:imports`
- **scope:** `time_tracking:imports` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The import ID. |
