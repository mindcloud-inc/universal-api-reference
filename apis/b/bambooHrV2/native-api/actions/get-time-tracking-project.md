# Get Time Tracking Project with BambooHR

Retrieves time tracking project from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-tracking/projects/:id`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Time Tracking Project](https://documentation.bamboohr.com/reference/get-project)

## Requirements

- **OAuth scopes:** `time_tracking:project`
- **scope:** `time_tracking:project` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The project ID. |
