# Search Invoices with HubSpot

Finds invoices in HubSpot.

## Endpoint

- **Method:** `POST`
- **Path:** `crm/v3/objects/invoices/search`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Body Pagination
- **Official documentation:** [Search Invoices](https://developers.hubspot.com/docs/api-reference/crm-invoices-v3/search/post-crm-v3-objects-invoices-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | no | A free-text query for invoice search. |
| `filterGroups` | body | `object<object>` | no | Provide the full HubSpot filterGroups array, for example [{"filters":[{"propertyName":"hs_object_id","operator":"EQ","value":"123"}]}]. |
| `filterGroups[].filters[]` | body | `array<object>` | no | The filters within a filter group. |
| `filterGroups[].filters[].propertyName` | body | `string` | no | The property name to filter on. |
| `filterGroups[].filters[].operator` | body | `list` | no | The operator to apply to the filter. Accepted values: `BETWEEN`, `CONTAINS_TOKEN`, `EQ`, `GT`, `GTE`, `HAS_PROPERTY`, `IN`, `LT`, `LTE`, `NEQ`, `NOT_CONTAINS_TOKEN`, `NOT_HAS_PROPERTY`, `NOT_IN`. |
| `filterGroups[].filters[].value` | body | `string` | no | The single comparison value for the filter. |
| `filterGroups[].filters[].values[]` | body | `array<string>` | no | Multiple comparison values for operators that accept arrays. |
| `filterGroups[].filters[].highValue` | body | `string` | no | The upper bound value for range filters. |
| `after` | body | `string` | no | The pagination cursor to continue a prior search. |
| `limit` | body | `number` | no | The number of results to return. |
| `sorts[]` | body | `array<string>` | no | The list of sort definitions. |
| `properties[]` | body | `array<string>` | no | The properties to include in each invoice result. |
