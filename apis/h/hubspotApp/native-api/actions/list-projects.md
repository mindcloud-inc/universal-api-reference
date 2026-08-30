# List Projects with HubSpot

## Endpoint

- **Method:** `GET`
- **Path:** `crm/objects/2026-03/projects`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [List Projects](https://developers.hubspot.com/docs/api-reference/latest/crm/objects/projects/guide)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `properties[]` | query | `array<string>` | no |
| `propertiesWithHistory[]` | query | `array<string>` | no |
| `associations[]` | query | `array<string>` | no |
| `archived` | query | `boolean` | no |
