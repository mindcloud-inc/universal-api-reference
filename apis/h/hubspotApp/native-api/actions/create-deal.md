# Create Deal with HubSpot

Creates a new deal in HubSpot.

## Endpoint

- **Method:** `POST`
- **Path:** `crm/v3/objects/deals`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Create Deal](https://developers.hubspot.com/docs/api-reference/crm-deals-v3/basic/post-crm-v3-objects-0-3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `properties` | body | `object` | no | The deal properties payload. |
| `properties.dealname` | body | `string` | no | The deal name. |
| `properties.dealstage` | body | `string` | no | The deal stage value. |
| `properties.pipeline` | body | `string` | no | The pipeline value. |
| `associations[]` | body | `array<object>` | no | Associations to create with the deal. |
| `associations[].to` | body | `object` | no | The association target. |
| `associations[].to.id` | body | `string` | no | The associated record ID. |
| `associations[].types[]` | body | `array<object>` | no | The association type definitions. |
| `associations[].types[].associationCategory` | body | `string` | no | The HubSpot association category. |
| `associations[].types[].associationTypeId` | body | `number` | no | The HubSpot association type ID. |
