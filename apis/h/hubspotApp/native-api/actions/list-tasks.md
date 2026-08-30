# List Tasks with HubSpot

## Endpoint

- **Method:** `GET`
- **Path:** `crm/objects/2026-03/tasks`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [List Tasks](https://developers.hubspot.com/docs/api-reference/latest/crm/activities/tasks/guide)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `properties[]` | query | `array<string>` | no |
| `propertiesWithHistory[]` | query | `array<string>` | no |
| `associations[]` | query | `array<string>` | no |
| `archived` | query | `boolean` | no |
