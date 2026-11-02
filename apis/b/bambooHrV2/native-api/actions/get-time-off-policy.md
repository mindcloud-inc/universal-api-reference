# Get Time Off Policy with BambooHR

Retrieves time off policy from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-off/policies/:id`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Time Off Policy](https://documentation.bamboohr.com/reference/get-time-off-policy)

## Requirements

- **OAuth scopes:** `time_off:policies`
- **scope:** `time_off:policies` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The time off policy ID. |
