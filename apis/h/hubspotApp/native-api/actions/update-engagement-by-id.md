# Update Engagement by ID with HubSpot

Updates an existing engagement record in HubSpot.

## Endpoint

- **Method:** `PATCH`
- **Path:** `crm/v3/objects/:engagementType/:engagementId`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Update Engagement by ID](https://developers.hubspot.com/docs/api-reference/crm-objects-v3/basic/patch-crm-v3-objects-objectType-objectId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `engagementType` | path | `string` | yes | HubSpot activity object type to update. Accepted values: `calls`, `communications`, `emails`, `meetings`, `notes`, `postal_mail`, `tasks`. |
| `engagementId` | path | `string` | yes | HubSpot record ID of the engagement to update. |
| `properties` | body | `object` | yes | Engagement property values keyed by HubSpot property name. |
| `idProperty` | query | `string` | no | Optional unique property name to use instead of the internal record ID. |
