# Search Orders with HubSpot

Finds orders in HubSpot.

## Endpoint

- **Method:** `POST`
- **Path:** `crm/v3/objects/orders/search`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Body Pagination
- **Official documentation:** [Search Orders](https://developers.hubspot.com/docs/api-reference/crm-orders-v3/search/post-crm-v3-objects-orders-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | no | A text query to search order records. |
| `filterGroups` | body | `object<object>` | no | Provide the full HubSpot filterGroups array, for example [{"filters":[{"propertyName":"hs_object_id","operator":"EQ","value":"123"}]}]. |
| `filterGroups[].filters[]` | body | `array<object>` | no | The filters inside each filter group. |
| `filterGroups[].filters[].propertyName` | body | `string` | no | The property to filter on. |
| `filterGroups[].filters[].operator` | body | `list` | no | The filter operator. Accepted values: `BETWEEN`, `CONTAINS_TOKEN`, `EQ`, `GT`, `GTE`, `HAS_PROPERTY`, `IN`, `LT`, `LTE`, `NEQ`, `NOT_CONTAINS_TOKEN`, `NOT_HAS_PROPERTY`, `NOT_IN`. |
| `filterGroups[].filters[].value` | body | `string` | no | The primary filter value. |
| `filterGroups[].filters[].highValue` | body | `string` | no | The high value for range filters. |
| `filterGroups[].filters[].values[]` | body | `array<string>` | no | Multiple filter values when supported. |
| `after` | body | `string` | no | The paging cursor token. |
| `limit` | body | `number` | no | The maximum number of orders to return. |
| `sorts[]` | body | `array<string>` | no | Sort expressions for the search results. |
| `properties[]` | body | `array<string>` | no | The order properties to include in each result. |
