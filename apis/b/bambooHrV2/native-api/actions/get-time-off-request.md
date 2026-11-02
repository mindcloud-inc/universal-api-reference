# Get Time Off Request with BambooHR

Retrieves time off request from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-off/requests/:id`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Time Off Request](https://documentation.bamboohr.com/reference/get-time-off-request)

## Requirements

- **OAuth scopes:** `time_off:requests`
- **scope:** `time_off:requests` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The time off request ID. |
| `returnActions` | query | `boolean` | no | Set to `true` to include the `_links` block naming the state transitions available to the caller for this time off request. Also accepts `1`, `yes` and `on`. Omitted from the response by default. |
