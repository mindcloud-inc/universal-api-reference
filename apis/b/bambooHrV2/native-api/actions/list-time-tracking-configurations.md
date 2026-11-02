# List Time Tracking Configurations with BambooHR

Lists time tracking configurations from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-tracking/configurations`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Time Tracking Configurations](https://documentation.bamboohr.com/reference/list-time-tracking-configurations)

## Requirements

- **OAuth scopes:** `time_tracking:configurations`
- **scope:** `time_tracking:configurations` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | OData v4 filter expression. Filterable fields: `name`, `type`, `timesheetType`. Example: `type eq 'GROUP' and timesheetType eq 'CLOCK'`. |
| `orderBy` | query | `string` | no | Sort expression like `name asc, createdAt desc`. Allowed fields: `name`, `createdAt`, `updatedAt`. |
| `select` | query | `string` | no | Comma-separated list of properties to return (sparse fieldsets). Send multiple values as a string separated by `,`. |
