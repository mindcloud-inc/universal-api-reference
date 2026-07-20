# Search Products with HubSpot

Finds products in HubSpot.

## Endpoint

- **Method:** `POST`
- **Path:** `crm/v3/objects/products/search`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Body Pagination
- **Official documentation:** [Search Products](https://developers.hubspot.com/docs/api-reference/crm-products-v3/search/post-crm-v3-objects-products-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | no | Full-text search string applied to the default searchable product properties. |
| `limit` | body | `number` | no | Maximum number of records to return in this search page. |
| `after` | body | `string` | no | Paging cursor for the next search page. |
| `properties[]` | body | `array<string>` | no | Properties to include in each returned product record. |
| `sorts[]` | body | `array<string>` | no | Sort clauses to apply to the search results. |
| `filterGroups` | body | `object<object>` | no | Provide the full HubSpot filterGroups array, for example [{"filters":[{"propertyName":"hs_object_id","operator":"EQ","value":"123"}]}]. |
| `filterGroups[].filters[]` | body | `array<object>` | no | Filters combined with AND semantics inside a filter group. |
| `filterGroups[].filters[].propertyName` | body | `string` | no | The product property name to filter on. |
| `filterGroups[].filters[].operator` | body | `list<string>` | no | The comparison operator to use for the filter. Accepted values: `BETWEEN`, `CONTAINS_TOKEN`, `EQ`, `GT`, `GTE`, `HAS_PROPERTY`, `IN`, `LT`, `LTE`, `NEQ`, `NOT_CONTAINS_TOKEN`, `NOT_HAS_PROPERTY`, `NOT_IN`. |
| `filterGroups[].filters[].value` | body | `string` | no | Single comparison value for the filter. |
| `filterGroups[].filters[].values[]` | body | `array<string>` | no | Multiple comparison values for IN and NOT_IN filters. |
| `filterGroups[].filters[].highValue` | body | `string` | no | Upper bound value for BETWEEN filters. |
