# Search Projects with HubSpot

## Endpoint

- **Method:** `POST`
- **Path:** `crm/objects/2026-03/projects/search`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Search Projects](https://developers.hubspot.com/docs/api-reference/latest/crm/objects/projects/search/search-projects)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `filterGroups[].filters[]` | body | `array<object>` | no |
| `filterGroups[].filters[].propertyName` | body | `string` | no |
| `filterGroups[].filters[].operator` | body | `string` | no |
| `filterGroups[].filters[].value` | body | `string` | no |
| `filterGroups[].filters[].values[]` | body | `array<string>` | no |
| `filterGroups[].filters[].highValue` | body | `string` | no |
| `after` | body | `string` | no |
| `limit` | body | `number` | no |
| `sorts[]` | body | `array<string>` | no |
| `properties[]` | body | `array<string>` | no |
