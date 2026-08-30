# Batch Read Projects with HubSpot

## Endpoint

- **Method:** `POST`
- **Path:** `crm/objects/2026-03/projects/batch/read`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Batch Read Projects](https://developers.hubspot.com/docs/api-reference/latest/crm/using-object-apis)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `inputs[]` | body | `array<object>` | yes |
| `properties[]` | body | `array<string>` | no |
| `propertiesWithHistory[]` | body | `array<string>` | no |
| `idProperty` | body | `string` | no |
