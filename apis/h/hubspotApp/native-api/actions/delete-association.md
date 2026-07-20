# Delete Association with HubSpot

Deletes an association between HubSpot records.

## Endpoint

- **Method:** `DELETE`
- **Path:** `crm/v4/objects/:objectType/:objectId/associations/:toObjectType/:toObjectId`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Delete Association](https://developers.hubspot.com/docs/api-reference/crm-associations-v4/basic/delete-crm-v4-objects-objectType-objectId-associations-toObjectType-toObjectId)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `objectType` | path | `string` | yes |
| `objectId` | path | `string` | yes |
| `toObjectType` | path | `string` | yes |
| `toObjectId` | path | `string` | yes |
