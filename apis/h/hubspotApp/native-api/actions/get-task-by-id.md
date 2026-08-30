# Get Task by ID with HubSpot

## Endpoint

- **Method:** `GET`
- **Path:** `crm/objects/2026-03/tasks/:taskId`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Get Task by ID](https://developers.hubspot.com/docs/api-reference/latest/crm/activities/tasks/guide)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `properties[]` | query | `array<string>` | no | — |
| `taskId` | path | `string` | yes | The HubSpot task record ID. |
| `propertiesWithHistory[]` | query | `array<string>` | no | — |
| `associations[]` | query | `array<string>` | no | — |
| `archived` | query | `boolean` | no | — |
