# Get Project by ID with HubSpot

## Endpoint

- **Method:** `GET`
- **Path:** `crm/objects/2026-03/projects/:projectId`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Get Project by ID](https://developers.hubspot.com/docs/api-reference/latest/crm/objects/projects/guide)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `string` | yes |
| `properties[]` | query | `array<string>` | no |
| `propertiesWithHistory[]` | query | `array<string>` | no |
| `associations[]` | query | `array<string>` | no |
| `archived` | query | `boolean` | no |
