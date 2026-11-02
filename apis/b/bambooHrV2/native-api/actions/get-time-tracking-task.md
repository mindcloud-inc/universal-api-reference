# Get Time Tracking Task with BambooHR

Retrieves time tracking task from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-tracking/tasks/:id`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Time Tracking Task](https://documentation.bamboohr.com/reference/get-task)

## Requirements

- **OAuth scopes:** `time_tracking:project`
- **scope:** `time_tracking:project` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The task ID. |
