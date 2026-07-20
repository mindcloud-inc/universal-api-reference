# List Properties with HubSpot

Retrieves properties from HubSpot.

## Endpoint

- **Method:** `GET`
- **Path:** `crm/v3/properties/:objectType`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [List Properties](https://developers.hubspot.com/docs/api-reference/crm-properties-v3/core/get-crm-v3-properties-objectType)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `objectType` | path | `string` | yes | The object type whose property definitions to list, such as companies or products. |
| `properties` | query | `string` | no | Comma-separated list of specific property names to include. Send multiple values as a string separated by `,`. |
| `dataSensitivity` | query | `list<string>` | no | The sensitivity category of properties to return. Accepted values: `highly_sensitive`, `non_sensitive`, `sensitive`. |
| `locale` | query | `string` | no | The locale to use for returned property labels and descriptions. |
| `archived` | query | `boolean` | no | Whether to return archived property definitions. |
