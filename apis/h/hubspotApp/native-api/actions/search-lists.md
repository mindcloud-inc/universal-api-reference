# Search Lists with HubSpot

Finds lists in HubSpot.

## Endpoint

- **Method:** `POST`
- **Path:** `crm/v3/lists/search`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Body Pagination
- **Official documentation:** [Search Lists](https://developers.hubspot.com/docs/api-reference/crm-lists-v3/lists/post-crm-v3-lists-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | no | Free-text query for list search. |
| `processingTypes[]` | body | `array<string>` | no | Optional list processing types filter. |
| `listIds[]` | body | `array<string>` | no | Optional list IDs filter. |
| `offset` | body | `number` | no | Pagination offset. |
| `count` | body | `number` | no | Page size. |
