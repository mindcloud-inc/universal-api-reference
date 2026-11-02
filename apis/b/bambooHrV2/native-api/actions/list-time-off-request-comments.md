# List Time Off Request Comments with BambooHR

Lists time off request comments from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-off/requests/:id/comments`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Time Off Request Comments](https://documentation.bamboohr.com/reference/list-time-off-request-comments)

## Requirements

- **OAuth scopes:** `time_off:requests`
- **scope:** `time_off:requests` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The time off request ID. |
