# Get Property Details with HubSpot

Retrieves property details from HubSpot.

## Endpoint

- **Method:** `GET`
- **Path:** `crm/v3/properties/:objectType/:propertyName`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Get Property Details](https://developers.hubspot.com/docs/api-reference/crm-properties-v3/core/get-crm-v3-properties-objectType-propertyName)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `objectType` | path | `string` | yes | The object type that owns the property definition, such as companies or products. |
| `propertyName` | path | `string` | yes | The internal name of the property to retrieve. |
| `dataSensitivity` | query | `list<string>` | no | The sensitivity category of the property to return. Accepted values: `highly_sensitive`, `non_sensitive`, `sensitive`. |
| `locale` | query | `string` | no | The locale to use for returned property labels and descriptions. |
| `archived` | query | `boolean` | no | Whether to return an archived property definition. |
