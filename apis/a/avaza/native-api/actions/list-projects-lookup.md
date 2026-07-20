# List Projects Lookup with Avaza

Retrieves projects lookup entries from Avaza.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/Project/Lookup`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [List Projects Lookup](https://api.avaza.com/#!/Project/ProjectLookup)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `TimesheetUserID` | query | `number` | no | Optionally Filter to the projects that the supplied UserID can add timesheets to |
| `CompanyIDFK` | query | `number` | no | Optionally Filter for a specific Company ID |
| `search` | query | `string` | no | Optional Search string to match against Project title and Customer name |
| `ProjectCode` | query | `string` | no | Optional string to exact match against Project Code |
