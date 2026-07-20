# Delete Property with HubSpot

Deletes an existing property from HubSpot.

## Endpoint

- **Method:** `DELETE`
- **Path:** `crm/v3/properties/:objectType/:propertyName`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Delete Property](https://developers.hubspot.com/docs/api-reference/crm-properties-v3/core/delete-crm-v3-properties-objectType-propertyName)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `objectType` | path | `string` | yes | The HubSpot object type that owns the property, such as deals, contacts, companies, or tickets. |
| `propertyName` | path | `string` | yes | The internal name of the property to archive/delete. |
