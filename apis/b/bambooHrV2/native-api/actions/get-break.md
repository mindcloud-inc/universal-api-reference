# Get Break with BambooHR

Retrieves break from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-tracking/breaks/:id`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Break](https://documentation.bamboohr.com/reference/get-break)

## Requirements

- **OAuth scopes:** `time_tracking:breaks`
- **scope:** `time_tracking:breaks` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The break ID. |
