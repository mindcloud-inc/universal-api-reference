# Get Time Off Category with BambooHR

Retrieves time off category from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-off/categories/:id`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Time Off Category](https://documentation.bamboohr.com/reference/get-time-off-category)

## Requirements

- **OAuth scopes:** `time_off:categories`
- **scope:** `time_off:categories` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The time off category ID. |
