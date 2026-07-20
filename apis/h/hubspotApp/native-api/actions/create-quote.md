# Create Quote with HubSpot

Creates a new quote in HubSpot.

## Endpoint

- **Method:** `POST`
- **Path:** `crm/v3/objects/quotes`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Create Quote](https://developers.hubspot.com/docs/api-reference/crm-quotes-v3/basic/post-crm-v3-objects-quotes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `properties` | body | `object` | no | The quote properties payload. |
| `properties.hs_title` | body | `string` | yes | The quote title shown in HubSpot. |
| `properties.hs_expiration_date` | body | `date` | yes | When the quote expires. |
| `properties.hs_template_type` | body | `string` | yes | Use the HubSpot CPQ template type. This action defaults to CPQ_QUOTE and does not support the legacy quote flow. |
| `properties.hs_slug` | body | `string` | no | Optional quote slug for the hosted quote URL. |
| `associations[]` | body | `array<object>` | no | Associations to create with the quote. |
| `associations[].to` | body | `object` | no | The association target. |
| `associations[].to.id` | body | `string` | no | The associated record ID. |
| `associations[].types[]` | body | `array<object>` | no | The association type definitions. |
| `associations[].types[].associationCategory` | body | `string` | no | The HubSpot association category. |
| `associations[].types[].associationTypeId` | body | `number` | no | The HubSpot association type ID. |
