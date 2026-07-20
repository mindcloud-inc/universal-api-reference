# Create Engagement with HubSpot

Creates a new engagement record in HubSpot.

## Endpoint

- **Method:** `POST`
- **Path:** `crm/v3/objects/:engagementType`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Create Engagement](https://developers.hubspot.com/docs/api-reference/crm-objects-v3/basic/post-crm-v3-objects-objectType)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `engagementType` | path | `string` | yes | HubSpot activity object type to create. Accepted values: `calls`, `communications`, `emails`, `meetings`, `notes`, `postal_mail`, `tasks`. |
| `properties` | body | `object` | yes | Engagement property values keyed by HubSpot property name. |
| `associations[]` | body | `array<object>` | no | Associations to create alongside the engagement. |
| `associations[].to.id` | body | `string` | no | HubSpot ID of the record to associate. |
| `associations[].types[]` | body | `array<object>` | no | Association type definitions for the linked record. |
| `associations[].types[].associationCategory` | body | `string` | no | Association category for the linked record. |
| `associations[].types[].associationTypeId` | body | `number` | no | Association type identifier for the linked record. |
