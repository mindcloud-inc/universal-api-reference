# Create Line Item with HubSpot

Creates a new line item in HubSpot.

## Endpoint

- **Method:** `POST`
- **Path:** `crm/v3/objects/line_items`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Create Line Item](https://developers.hubspot.com/docs/api-reference/crm-line-items-v3/guide)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `properties` | body | `object` | yes | Line item property values object. |
| `associations[]` | body | `array<object>` | no | Optional associations for the new line item. |
