# List Projects with ArcSite

Retrieves project records from your ArcSite organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects`
- **Base URL:** `https://api.arcsite.com/v1`
- **Official documentation:** [List Projects](https://dev.arcsite.com/#query-projects)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `created_at_begin` | query | `date` | no | Filter by project creation start date in UTC ISO 8601 format. |
| `created_at_end` | query | `date` | no | Filter by project creation end date in UTC ISO 8601 format. |
