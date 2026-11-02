# List Time Tracking Time Clocks with BambooHR

Lists time tracking time clocks from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-tracking/time-clocks`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Time Tracking Time Clocks](https://documentation.bamboohr.com/reference/list-time-tracking-time-clocks)

## Requirements

- **OAuth scopes:** `time_tracking:time_clocks`
- **scope:** `time_tracking:time_clocks` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | OData v4 filter expression. Filterable fields: `name`, `serialNumber`, `type`, `timezone`. Example: `type eq 'TIME_CLOCK'`. |
| `orderBy` | query | `string` | no | Sort expression like `name asc, serialNumber desc`. Allowed fields: `name`, `serialNumber`, `type`, `timezone`. Defaults to `name asc`. |
| `select` | query | `string` | no | Comma-separated list of properties to return (sparse fieldsets). Send multiple values as a string separated by `,`. |
