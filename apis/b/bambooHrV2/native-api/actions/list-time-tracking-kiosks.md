# List Time Tracking Kiosks with BambooHR

Lists time tracking kiosks from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-tracking/kiosks`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Time Tracking Kiosks](https://documentation.bamboohr.com/reference/list-time-tracking-kiosks)

## Requirements

- **OAuth scopes:** `time_tracking:kiosks`
- **scope:** `time_tracking:kiosks` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | OData v4 filter expression. Filterable fields: `name`, `lastUsed`, `createdAt`, `updatedAt`. Example: `name eq 'Front Desk Kiosk'`. |
| `orderBy` | query | `string` | no | Sort expression like `name asc, createdAt desc`. Allowed fields: `name`, `lastUsed`, `createdAt`, `updatedAt`. Defaults to `name asc`. |
| `select` | query | `string` | no | Comma-separated list of properties to return (sparse fieldsets). Send multiple values as a string separated by `,`. |
