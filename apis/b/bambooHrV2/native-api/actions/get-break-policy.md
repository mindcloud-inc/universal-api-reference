# Get Break Policy with BambooHR

Retrieves break policy from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-tracking/break-policies/:id`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Break Policy](https://documentation.bamboohr.com/reference/get-break-policy)

## Requirements

- **OAuth scopes:** `time_tracking:breaks`
- **scope:** `time_tracking:breaks` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The break policy ID. |
| `includeCounts` | query | `boolean` | no | Include employee and break counts |
