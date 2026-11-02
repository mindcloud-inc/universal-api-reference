# List Employee Break Policies with BambooHR

Lists employee break policies from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-tracking/employees/:id/break-policies`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Employee Break Policies](https://documentation.bamboohr.com/reference/list-employee-break-policies)

## Requirements

- **OAuth scopes:** `time_tracking:breaks`
- **scope:** `time_tracking:breaks` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The internal employee ID. |
