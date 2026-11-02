# List Time Tracking Shift Differentials with BambooHR

Lists time tracking shift differentials from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-tracking/shift-differentials`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Time Tracking Shift Differentials](https://documentation.bamboohr.com/reference/list-shift-differentials)

## Requirements

- **OAuth scopes:** `time_tracking:shift_differentials`
- **scope:** `time_tracking:shift_differentials` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | OData v4 filter expression. Filterable fields: `name`, `rate`, `rateType`, `archived`. |
| `sort` | query | `string` | no | Sort expression like `name asc, createdAt desc`. Allowed fields: `name`, `createdAt`, `updatedAt`. |
