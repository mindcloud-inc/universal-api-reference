# Update Custom Object Record with HubSpot

Updates a custom object record in HubSpot.

## Endpoint

- **Method:** `PATCH`
- **Path:** `crm/v3/objects/:objectType/:objectId`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Update Custom Object Record](https://developers.hubspot.com/docs/api-reference/crm-custom-objects-v3/guide)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `objectType` | path | `string` | yes | Custom object type ID or fully qualified name, for example `2-56303805`. |
| `objectId` | path | `string` | yes | HubSpot custom object record ID to update. |
| `properties` | body | `object` | yes | Object of custom object properties to update, for example `{"source_app":"cirra"}`. |
| `idProperty` | query | `string` | no | Unique property used to identify the record instead of the internal record ID. |
