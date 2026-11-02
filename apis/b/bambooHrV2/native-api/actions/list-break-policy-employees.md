# List Break Policy Employees with BambooHR

Lists break policy employees from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-tracking/break-policies/:id/employees`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Break Policy Employees](https://documentation.bamboohr.com/reference/list-break-policy-employees)

## Requirements

- **OAuth scopes:** `time_tracking:breaks`
- **scope:** `time_tracking:breaks` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The break policy ID. |
