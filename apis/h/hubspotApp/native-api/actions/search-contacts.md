# Search Contacts with HubSpot

Finds contacts in HubSpot.

## Endpoint

- **Method:** `POST`
- **Path:** `crm/v3/objects/contacts/search`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Body Pagination
- **Official documentation:** [Search Contacts](https://developers.hubspot.com/docs/api-reference/crm-contacts-v3/search/post-crm-v3-objects-contacts-search)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | no | The text to search across default searchable contact properties. |
| `filterGroups[].filters[]` | body | `array<object>` | no | Add a Property, Operator, and Value to filter your search results. Add additional filters in the same group for AND logic. |
| `filterGroups[].filters[].propertyName` | body | `list<string>` | no | The contact property to filter on. |
| `filterGroups[].filters[].operator` | body | `list` | no | The comparison operator used by the filter. Accepted values: `BETWEEN`, `CONTAINS_TOKEN`, `EQ`, `GT`, `GTE`, `HAS_PROPERTY`, `IN`, `LT`, `LTE`, `NEQ`, `NOT_CONTAINS_TOKEN`, `NOT_HAS_PROPERTY`, `NOT_IN`. |
| `filterGroups[].filters[].value` | body | `string` | no | The primary comparison value used by the filter. |
| `filterGroups[].filters[].values[]` | body | `array<string>` | no | Multiple comparison values for list-style operators. |
| `filterGroups[].filters[].highValue` | body | `string` | no | The upper bound used by range filters. |
| `after` | body | `string` | no | The paging cursor for the next set of search results. |
| `limit` | body | `number` | no | The maximum number of contacts to return. |
| `sorts[]` | body | `array<string>` | no | Fields used to sort the returned contacts. |
| `properties` | body | `list<string>` | no | Select the contact properties to include in the response. Send multiple values as a array. |
