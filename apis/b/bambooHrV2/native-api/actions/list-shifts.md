# List Shifts with BambooHR

Lists shifts from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/scheduling/shifts`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Shifts](https://documentation.bamboohr.com/reference/scheduling-list-shifts)

## Requirements

- **OAuth scopes:** `scheduling:shifts time_tracking`
- **scope:** `scheduling:shifts, time_tracking` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | query | `string` | no | Filter by shift IDs, as either a comma-separated string (e.g. id1,id2) or an array. If provided, other filters are ignored. Send multiple values as a string separated by `,`. |
| `start` | query | `date` | no | Start datetime for the shift window (ISO-8601 datetime string). Required if ids not provided. |
| `end` | query | `date` | no | End datetime for the shift window (ISO-8601 datetime string). Required if ids not provided. |
| `employeeIds` | query | `string` | no | Filter by employee IDs, as either a comma-separated string (e.g. 10,20) or an array. Use the string "null" as a value to include unassigned shifts (e.g. employeeIds=10,null). Send multiple values as a string separated by `,`. |
| `scheduleIds` | query | `string` | no | Filter by schedule IDs, as either a comma-separated string (e.g. id1,id2) or an array. Send multiple values as a string separated by `,`. |
| `statuses` | query | `list<string>` | no | Filter by shift statuses, as either a comma-separated string (e.g. planned,published) or an array. Accepted values: `cancelled`, `deleted`, `planned`, `published`. Send multiple values as a string separated by `,`. |
