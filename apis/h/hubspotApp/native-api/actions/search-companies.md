# Search Companies with HubSpot

Finds companies in HubSpot.

## Endpoint

- **Method:** `POST`
- **Path:** `crm/v3/objects/companies/search`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Body Pagination
- **Official documentation:** [Search Companies](https://developers.hubspot.com/docs/api-reference/crm-companies-v3/search/post-crm-v3-objects-companies-search)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filterGroups[].filters[]` | body | `array<object>` | no | — |
| `filterGroups[].filters[].propertyName` | body | `string<string>` | no | — |
| `query` | body | `string` | no | The text to search across default searchable company properties. |
| `after` | body | `string` | no | The paging cursor for the next set of search results. |
| `filterGroups[].filters[].operator` | body | `list` | no | — |
| `filterGroups[].filters[].value` | body | `string` | no | — |
| `limit` | body | `number` | no | The maximum number of companies to return. |
| `filterGroups[].filters[].values[]` | body | `array<string>` | no | — |
| `sorts[]` | body | `array<string>` | no | Fields used to sort the returned companies. |
| `filterGroups[].filters[].highValue` | body | `string` | no | — |
| `properties[]` | body | `array<string>` | no | Company properties to include in the response. |
| `filterGroups` | body | `object<object>` | no | Provide the full HubSpot filterGroups array, for example [{"filters":[{"propertyName":"hs_object_id","operator":"EQ","value":"123"}]}]. |
| `properties[]` | body | `array<string>` | no | — |
