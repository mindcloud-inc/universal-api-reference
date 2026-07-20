# Search Deals with HubSpot

Finds deals in HubSpot.

## Endpoint

- **Method:** `POST`
- **Path:** `crm/v3/objects/deals/search`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Body Pagination
- **Official documentation:** [Search Deals](https://developers.hubspot.com/docs/api-reference/crm-deals-v3/search/post-crm-v3-objects-0-3-search)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | no | The text query to match across searchable deal properties. |
| `filterGroups` | body | `object` | no | Provide the full HubSpot filterGroups array, for example [{"filters":[{"propertyName":"dealname","operator":"EQ","value":"example deal"}]}]. |
| `filterGroups[].filters[]` | body | `array` | no | Filters to apply within a filter group. |
| `filterGroups[].filters[].propertyName` | body | `string` | no | The property name to filter on. |
| `filterGroups[].filters[].operator` | body | `list` | no | The operator to apply to the filter. Accepted values: `BETWEEN`, `CONTAINS_TOKEN`, `EQ`, `GT`, `GTE`, `HAS_PROPERTY`, `IN`, `LT`, `LTE`, `NEQ`, `NOT_CONTAINS_TOKEN`, `NOT_HAS_PROPERTY`, `NOT_IN`. |
| `filterGroups[].filters[].value` | body | `string` | no | A single value for the filter. |
| `filterGroups[].filters[].highValue` | body | `string` | no | The upper bound value when using the BETWEEN operator. |
| `filterGroups[].filters[].values[]` | body | `array<string>` | no | Multiple values for IN or NOT_IN filters. |
| `sorts[]` | body | `array` | no | Sorting rules to apply to the search results. |
| `sorts[].propertyName` | body | `string` | no | The property name to sort by. |
| `sorts[].direction` | body | `string` | no | The sort direction. |
| `properties[]` | body | `array<string>` | no | Deal property names to return in the response. |
